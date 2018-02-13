public class Solution {
   	public boolean hotel(ArrayList<Integer> arrive, ArrayList<Integer> depart, int K) {
		Collections.sort(arrive);
		Collections.sort(depart);
		int roomsRequired=0,i=0,j=0;
		while(i<arrive.size()  && j<arrive.size() && roomsRequired<=K){
			if(arrive.get(i)<depart.get(j) ){
				i++;
				roomsRequired++;
			}else{
				j++;
				roomsRequired--;
			}
		}
		if(roomsRequired<=K){
			return true;
		}else{
			return false;
		}
	}
}
