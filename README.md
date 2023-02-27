# anagram
int remAnagram(string str1, string str2)
{
// Your code goes here
int counter1[26]={0};
int counter2[26]={0};
for(int i=0;i<str1.size();i++){
    counter1[str1[i]-'a']++;
}
for(int i=0;i<str2.size();i++){
    counter2[str2[i]-'a']++;
    
}
int ans=0;
for(int i=0;i<26;i++){
    ans+=abs(counter1[i]-counter2[i]);
    
}
return ans;
};
