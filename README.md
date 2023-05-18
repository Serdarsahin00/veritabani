# veritabani
   static  void balonpozisyonubul(int N,int M){
     Node head =new Node(1);
     Node next=head;
        for (int i = 2; i <=N; i++) {
            Node newnode=new Node(i);
            next.next=newnode;
            next=newnode;
        }
       
        next.next=head;
        Node baslangıc = head; 
        while (baslangıc.next!=baslangıc) {            
            for (int i = 1; i < M; i++) { 
                next=baslangıc;
                baslangıc=baslangıc.next;
            }
            next.next=baslangıc.next;
            baslangıc=next.next;
        }
        System.out.println("patlamayan balonun pozisyonu "+baslangıc.data);
    }
   
