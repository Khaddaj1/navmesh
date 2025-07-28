using UnityEngine;
using UnityEngine.AI;
public class agent : MonoBehaviour
{

    public Transform player;
    private NavMeshAgent Agent_elman;

    // Start is called once before the first execution of Update after the MonoBehaviour is created
    void Start()
    {
        Agent_elman = GetComponent<NavMeshAgent>();
    }

    // Update is called once per frame
    void Update()
    {
        
        if ((player.position - Agent_elman.transform.position).magnitude <= 3)
        {
            Agent_elman.destination = player.position;
        }
    }
}
