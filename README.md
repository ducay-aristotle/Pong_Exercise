# Pong_Exercise
The goal of this is to build the game pong from start to finish while also getting familiar working in C# and the unity engine.

## Skills Aquired/Learned
- Fundamentals of using C#
- Fundamentals with working inside the Unity Engine.
- Fundamentals with creating and using prefabs



## Source Code:
Source code for Player Paddle:

    using System.Collections;
    using System.Collections.Generic;
    using UnityEngine;

    public class Paddle : MonoBehaviour {

    [SerializeField]
    float speed;

    float height;

    string input;
    public bool isRight;

	// Use this for initialization
	void Start ()
    {
        height = transform.localScale.y;
        speed = 5f;
	}


    public void Init(bool isRightPaddle)
    {
        isRight = isRightPaddle;

        Vector2 pos = Vector2.zero;

        if (isRightPaddle)
        {
            //Place Paddle on Right side of Screen
            pos = new Vector2(GameManager.topRight.x, 0);
            pos -= Vector2.right * transform.localScale.x; //Move a bit to the left

            input = "PaddleRight";
        }



# what needs fixing
- Fix the score board to reset the ball and add points to whomever scored.


