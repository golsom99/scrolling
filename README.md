# scrolling
this is scrolling
#include "defs.h"


SDL_Rect scroll_function(SDL_Rect *camera , int *b , SDL_Surface *ecran , SDL_Surface *background , int *continu)
{

if(b[0]==1)
{

*continu=0;
}

switch(b[1])
{


case 0 :
SDL_BlitSurface(background, camera, ecran, NULL);
SDL_Flip(ecran);
break ;

case 1 :

camera->x += speed;


SDL_BlitSurface(background, camera, ecran, NULL);
SDL_Flip(ecran);
break ;




}





switch(b[2])
{

case 0 :
SDL_BlitSurface(background, camera, ecran, NULL);
SDL_Flip(ecran);
break ;


case 1 :

camera->x -= speed;


SDL_BlitSurface(background, camera, ecran, NULL);

SDL_Flip(ecran);

break ;

}



return *camera ;


}



