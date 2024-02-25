# generacion-de-tonos-usando-PSoC-5LP-

#include <project.h>

int aumentar=0;

CY_ISR(tempo)
{
    if(aumentar ==1)//Do4
    {
    PWM_WritePeriod(3822);
    PWM_WriteCompare(1911);
   
    }
    
    if(aumentar ==2)//Re4
    {
    PWM_WritePeriod(3405);
    PWM_WriteCompare(1702);
    
    }
    
    if(aumentar ==3)//Mi4
    {
    PWM_WritePeriod(3033);
    PWM_WriteCompare(1516);
    
    }
    
    if(aumentar ==4)//Fa4
    {
    PWM_WritePeriod(2863);
    PWM_WriteCompare(1431);
   
    }
    
    if(aumentar ==5)//Sol4
    {
    PWM_WritePeriod(2551);
    PWM_WriteCompare(1275);
    
    }
    
    if(aumentar ==6)//La4
    {
    PWM_WritePeriod(2272);
    PWM_WriteCompare(1136);
    
    }
    if(aumentar ==7)//Si4
    {
    PWM_WritePeriod(2024);
    PWM_WriteCompare(1012);
   
    }
    
    if(aumentar ==8)//Do5
    {
    PWM_WritePeriod(1911);
    PWM_WriteCompare(955);
    
    aumentar=0;
    }
    
    aumentar++;
}
int main()
{
    CyGlobalIntEnable;
    
PWM_Start();
Clock_Start();
timer_clock_Start();
Timer_Start();


isrTempo_StartEx(tempo);
    for(;;)
    {
        
    }
}
informacion utilizada en este proyecto:https://www.undiaunacancion.es/compas-44-explorando-sus-caracteristicas-y-ejemplos/  https://www.sonidosbinaurales.com/frecuencias-de-las-notas-musicales/  https://www.infineon.com/dgdl/Infineon-Component_PWM_V3.30-Software+Module+Datasheets-v03_03-EN.pdf?fileId=8ac78c8c7d0d8da4017d0e80682d120d  https://www.infineon.com/dgdl/Infineon-Component_Timer_V2.70-Software+Module+Datasheets-v02_08-EN.pdf?fileId=8ac78c8c7d0d8da4017d0ea711f72733
