package music;
import javax.sound.midi.*;
public class exp {
	public static void main(String[] a){
		exp e=new exp();
		e.play();
	}
	public void play(){
		try{
			Sequencer sq=MidiSystem.getSequencer();
			sq.open();
			Sequence s=new Sequence(Sequence.PPQ,4);
			Track track=s.createTrack();
			ShortMessage a=new ShortMessage();
			a.setMessage(144,1,127,4);
			track.add(new MidiEvent(a,16));
			sq.setSequence(s);
			sq.start();
		}
		catch(Exception e){
			
		}

		
	}
	

}

