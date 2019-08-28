    public class TestUtils
    {
        private static readonly Random RandomGenerator = new Random((int)DateTime.Now.Ticks);

        /// <summary>
        /// Generate Random Number between two numbers
        /// </summary>
        /// <param name="min">mininum number</param>
        /// <param name="max">max number</param>
        /// <returns>Int</returns>
        public static int GetRandomInt(int min = 0, int max = int.MaxValue)
        {
            return RandomGenerator.Next(min, max);
        }

        /// <summary>
        /// Generate a random phone Number
        /// </summary>
        /// <param name="mobile">boolean, if true returns a mobile phone number, else returns a local phone number</param>
        /// <returns>int</returns>
        public static int RandomPhoneNumber(bool mobile)
        {
            string phone = "";

            if (mobile) { 
                var list = new List<int> { 1, 2, 3, 6 };
                int index = RandomGenerator.Next(list.Count);

                phone = string.Concat("9", list[index].ToString(), GetRandomInt(1111111, 9999999).ToString());
            }
            else
            {
                phone = string.Concat("2", GetRandomInt(11111111, 99999999).ToString());
            }

            return Convert.ToInt32(phone);
        }

        /// <summary>
        /// Generate a random string
        /// </summary>
        /// <param name="size">number of characters</param>
        /// <returns>string</returns>
        public static string RandomString(int size)
        {
            StringBuilder builder = new StringBuilder();
            char ch;
            for (int i = 0; i < size; i++)
            {
                ch = Convert.ToChar(Convert.ToInt32(Math.Floor(26 * RandomGenerator.NextDouble() + 65)));
                builder.Append(ch);
            }

            return builder.ToString();
        }

        /// <summary>
        /// Generate a random email
        /// </summary>
        /// <returns>string</returns>
        public static string RandomEmail()
        {
            // I swear that this was a random choice.
            return string.Concat(RandomString(8), "@", RandomString(4), ".com");
        }

        /// <summary>
        /// Generate a random boolean value, either true or false
        /// </summary>
        /// <returns>bool</returns>
        public static bool RandomBool()
        {
            return GetRandomInt(0, 1) == 0;
        }
    }
