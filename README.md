# Armstrong
Armstrong's numbers


    public class Mqtt 
    {
        static int size = 5;
        static int depth = 0;
        static int maxDepth = 0;
        static int[] number = new int[size];
        
        public static void main(String[] args) 
        {        
            numset();
        }
    
        static void numset()
        {
            depth++;
            for(int i = 0; i <= 9; i++)
            {
                if(depth < size)
                {
                    numset();
                }
                
                if(size - depth > maxDepth)
                {
                    maxDepth = size - depth;
                }
                
                number[depth - 1] = i;
                halb(maxDepth);
            }
            depth--;
        }
        
        static void halb(int j)
        {
            int sum = 0;
            Integer num = 0;
            
            for(int i = 0; i < number.length; i++)
            {
                sum += Math.pow(number[i], j);
                num += (int) (number[i] * Math.pow(10, i));
            }
            
            if(sum == num)
            {
                String s = num.toString();
                System.out.println(s);
            }
        }    
    }
    
    Clash of Operators
    
