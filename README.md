class Solution {
    void reorderlist(Node head) {
     ArrayList<Integer> a=new ArrayList<Integer>();
        Node cur=head;
        while(cur!=null)
        {
            a.add(cur.data);
            cur=cur.next;
        }
        cur=head;
        int d=a.size()-1,k=0;
        for(int i=0;i<a.size();i++)
        {
            if(i%2==0){
            cur.data=a.get(k);
            cur=cur.next;
            k++;
            }
            else{
                cur.data=a.get(d);
                cur=cur.next;
                d--;
            }
        }
    }
}
