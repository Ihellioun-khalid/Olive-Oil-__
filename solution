/*********************************************
 * OPL 12.6.0.0 Model
 * Olive Oil
 *********************************************/

//Make sure you use c[i] to access the i-th cost 
//and do not remove/change the following line
float c[1..4] = [200, 200, 2.1, 1.7];
// c[1] = 200 = 4*300 - 1000
// c[2] = 200 = 6*200 - 1000
// c[3] = 2.1 = -4 + 6*0.6 + 10*0.3 - 0.5
// c[4] = 1.7 = -6 +10*0.8 - 0.3

dvar float x;
dvar float y;
dvar float z;
dvar float t;

maximize c[1]*x + c[2]*y + c[3]*z + c[4]*t;

subject to {
    300*x             - z <= 3000;
        200*y - t + 0.6* z <= 3000;
            0.8*t + 0.3 *z <= 2000;
            x>=0;
            y>=0;
            z>=0;
            t>=0;
           300*x             - z>=0; 
           200*y - t + 0.6* z>=0;
           0.8*t + 0.3 *z>=0;
}

/* Affichage de la solution */
execute {
  writeln("Post-traitement: ");
  writeln("La valeur de l'objectif est de "+cplex.getObjValue());
} 