# IGNITION
MUSEO INTERACTIVO
using UnityEngine;
using System.Collections;
using UnityEngine.SceneManagement;

public class universe : MonoBehaviour {

	// Use this for initialization
	public void SiguienteEscena () {
        SceneManager.LoadScene("dino");
	}
	
	// Update is called once per frame
	void Update () {
	
	}
}
	// Use this for initialization
    }
    public class universe : MonoBehaviour {

	// Use this for initialization
	public void SiguienteEscena () {
        SceneManager.LoadScene("UNIVERSE");
	}
	
	
DINOSAURIO
using UnityEngine;
using System.Collections;

public class AllosaurusCameraScript : MonoBehaviour {

	public GameObject target;
	public float turnSpeed=.2f;
	
	void FixedUpdate(){
		transform.position = Vector3.Lerp (transform.position,target.transform.position,Time.deltaTime);
		transform.rotation = Quaternion.Lerp (transform.rotation,target.transform.rotation,Time.deltaTime*turnSpeed);
	}
}







	public GameObject allosaurusCamera;
	public GameObject[] allosaurus;


	public void AllosaurusSelect(int alloNum){
		AllosaurusCameraScript frogcamerascript=allosaurusCamera.GetComponent<AllosaurusCameraScript>();
		frogcamerascript.target = allosaurus [alloNum];
	}
}



	(CARD BOARD)
	public static Cardboard SDK {
    get {
      if (sdk == null) {
        if (Application.isEditor && !Application.isPlaying) {
          // Let the editor scripts access the object through this property.
          sdk = UnityEngine.Object.FindObjectOfType<Cardboard>();
        } else {
          Debug.LogError("No Cardboard instance found.  Ensure one exists in the scene, or call"
              + "Cardboard.Create() at startup to generate one.\n"
              + "If one does exist but hasn't called Awake() yet, "
              + "then this error is due to order-of-initialization.\n"
              + "In that case, consider moving "
              + "your first reference to Cardboard.SDK to a later point in time.\n"
              + "If exiting the scene, this indicates that the Cardboard object has already "
              + "been destroyed.");
        }
      }
      return sdk;
    }
  }
  private static Cardboard sdk = null;

  /// Generate a Cardboard instance.  Takes no action if one already exists.
  public static void Create() {
    if (sdk == null && UnityEngine.Object.FindObjectOfType<Cardboard>() == null) {
      Debug.Log("Creating Cardboard object");
      var go = new GameObject("Cardboard", typeof(Cardboard));
      go.transform.localPosition = Vector3.zero;
      // sdk will be set by Cardboard.Awake().
    }
  }

 
        
