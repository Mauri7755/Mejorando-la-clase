# Mejorando-la-clase
using System;
using System.Collections;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApplication69
{
    class Calificaciones
    {
        int Salon, Alum, Califi;
        ArrayList Listas;
        ArrayList Lista1;
        public void Calificacion()
        {
            Listas = new ArrayList();
            Lista1 = new ArrayList();

        }
        public void Operacion()
        {
            Console.WriteLine("¿Cuantas clases son?");
            Salon = int.Parse(Console.ReadLine());
           
            for(int n=0;n<Salon;n++)
            {
                Console.WriteLine("¿Cuantos hay en cada grupo: {0}?", n+1);
                Alum = int.Parse(Console.ReadLine());
                Listas.Add(Alum);
            }

            for (int n = 0; n < Listas.Count; n++)
            {
                Console.WriteLine("Ingresa calificaciones de cada grupo:");
                Califi = int.Parse(Console.ReadLine());
                Lista1.Add(Califi);

            }
        }

        public void Imprimir()
        {
            Console.WriteLine("Cantidad de alumnos por grupo:");
            foreach(var pug in Listas)
            {
                Console.WriteLine(pug);
            }

            Console.WriteLine("Calificacion por grupo:");
            foreach (var pong in Lista1)
            {
                Console.WriteLine(pong);
            }

            Console.ReadKey();
        }
    
            static void Main(string[] args)
        {
            Calificaciones m = new Calificaciones();
            m.Operacion();
            Console.Clear();
            m.Imprimir();
            Console.ReadKey();
        }
      }
    }
