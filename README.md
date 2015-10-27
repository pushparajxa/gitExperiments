MZ format tagged (compressed)
-----------------------------

We support three different implementations of LZ4:
* Native: Depends on native library (automatically used, included in mzp).
* Java Unsafe: Depends on Java Unsafe operations (non checked memory access in JVM).
* Safe: Pure java implementation.
    
No additional properties should be needed when running ECs on HPUX.
    
Properties that effect LZ4 compression.
    
Property: mz.tag.compression.lz4.allow_native
Default: true
Description: Enables use of native LZ4 compression on supported platforms (currently only Linux).
    
Property: mz.tag.compression.lz4.allow_java_unsafe
Default: true
Description: Enables use of Java Unsafe LZ4 compression on all platforms.
    
Property: mz.tag.compression.lz4.hpux_jvm_crash_workaround
Default: true
Description: Will force properties mz.tag.compression.lz4.allow_native and mz.tag.compression.lz4.allow_java_unsafe to false on HP/UX.
    
To enable Java Unsafe implementation on HP/UX set hpux_jvm_crash_workaround to false and allow_java_unsafe to true.

# gitExperiments
