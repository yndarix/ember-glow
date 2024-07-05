using System;

namespace EmberGlowApp
{
    class Program
    {
        static void Main(string[] args)
        {
            // Creating an instance of the EmberGlow class
            EmberGlow ember = new EmberGlow();
            ember.LightUp();

            // Displaying a message about the current state
            Console.WriteLine("Current Ember State: " + ember.CurrentState);

            // Changing the state of the ember
            ember.Dim();
            Console.WriteLine("Current Ember State: " + ember.CurrentState);

            // Re-lighting the ember
            ember.LightUp();
            Console.WriteLine("Current Ember State: " + ember.CurrentState);
        }
    }

    // A class to simulate an ember that glows and dims
    public class EmberGlow
    {
        // Property to track the current state of the ember
        public string CurrentState { get; private set; }

        // Constructor to initialize the ember state
        public EmberGlow()
        {
            CurrentState = "Dim";
        }

        // Method to light up the ember
        public void LightUp()
        {
            CurrentState = "Glowing";
            Console.WriteLine("The ember is now glowing.");
        }

        // Method to dim the ember
        public void Dim()
        {
            CurrentState = "Dim";
            Console.WriteLine("The ember is now dim.");
        }
    }
}
