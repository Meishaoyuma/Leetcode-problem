class Solution {
    List<List<Integer>> ans;
    public List<List<Integer>> combinationSum3(int k, int n) {
        int bits = 0;
        ans= new ArrayList<>();
        dfs(bits,k,n,0,new ArrayList<Integer>());
        return ans;
    }
    void dfs( int bits, int k, int n, int sum ,List<Integer> list){
        if(sum>n){
            return;
        }
        if(list.size()==k && sum == n){
            ans.add(new ArrayList<>(list));
            return;
        }
        for(int i =1;i<10;i++){
            if( ((1<<i) & bits)!=0){
                continue;
            }
            list.add(i);
            bits|=(1<<i);
            dfs(bits,k,n,sum+i,list);
            list.remove(list.size()-1);
        } 
    }
}
