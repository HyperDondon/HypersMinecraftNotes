# Rising Particles

Supposed random formula for the direction of rising particles (e.g. flame particles):

```java
this.x += (double)((this.random.nextFloat() - this.random.nextFloat()) * 0.05F);  
this.y += (double)((this.random.nextFloat() - this.random.nextFloat()) * 0.05F);  
this.z += (double)((this.random.nextFloat() - this.random.nextFloat()) * 0.05F);  
this.lifetime = (int)(8.0D / (Math.random() * 0.8D + 0.2D)) + 4;
```

Found inside constructor of net.minecraft.client.particle.RisingParticle


tick() method found in the net.minecraft.client.particle.Particle ~={clear}class
```java
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


These lines indicates the the coordinate variables that end with "d" mean the friction, not sure yet.
```java
this.xd *= (double)this.friction;  
this.yd *= (double)this.friction;  
this.zd *= (double)this.friction;
```