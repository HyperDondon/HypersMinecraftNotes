# Rising Particles

Supposed random formula for the direction of rising particles (e.g. flame particles):
	~={yellow} (8.0D / (Math.random() * 0.8D + 0.2D)) + 4
	~={clear} Class: ~={cyan} net.minecraft.client.particle.RisingParticle
 **~={clear}This was found inside the constructor.


~={clear}tick() method found in the ~={cyan}net.minecraft.client.particle.Particle ~={clear}class
```
public void tick() {  
   this.xo = this.x;  
   this.yo = this.y;  
   this.zo = this.z;  
   if (this.age++ >= this.lifetime) {  
      this.remove();  
   } else {  
      this.yd -= 0.04D * (double)this.gravity;  
      this.move(this.xd, this.yd, this.zd);  
      if (this.speedUpWhenYMotionIsBlocked && this.y == this.yo) {  
         this.xd *= 1.1D;  
         this.zd *= 1.1D;  
      }  
  
      this.xd *= (double)this.friction;  
      this.yd *= (double)this.friction;  
      this.zd *= (double)this.friction;  
      if (this.onGround) {  
         this.xd *= (double)0.7F;  
         this.zd *= (double)0.7F;  
      }  
  
   }  
}

``` 


This line
```
this.xd *= (double)this.friction;  
this.yd *= (double)this.friction;  
this.zd *= (double)this.friction;
```
indicates the the coordinate variables that end with d mean the friction, not sure yet.