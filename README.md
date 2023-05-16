# Verification-of-Sampling-Theorem

The sampling theorem essentially says that a signal has to be sampled at least with twice the
frequency of the original signal. Since signals and their respective speed can be easier
expressed by frequencies, most explanations of artifacts are based on their representation in
the frequency domain. The sampling frequency required by the sampling theorem is called
the Nyquist frequency.
If the highest frequency contained in an analog signal xa( t ) is Fmax = B and the signal is
sampled at a rate Fs&gt;2Fmax = 2B. then xa(t)can be exactly recovered from its sample values
using the interpolation function

Thus xa(t) may be expressed as

Where xa (n/Fs ) = xa (n T ) = x (n) are the samples of xa(t ).
When the sampling of xa(t)is performed at the minimum sampling rate Fs= 2B, the
reconstruction formula in

The sampling rate FN = 2B = 2Fmax is called the Nyquist rate.


Matlab Code:
T=0.02;
m=0:0.0004:0.02;
n=2*sin(2*pi*m/T);
subplot(2,2,1);
plot(m,n,&#39;b&#39;);
xlabel(&#39;m&#39;);
ylabel(&#39;n&#39;);
title(&#39;Continuous Signal&#39;);

ts1=0.002;
m1=0:1:10;
n1=2*sin(2*pi*m1*ts1/T);
subplot(2,2,2);
stem(m1,n1,&#39;b&#39;);
xlabel(&#39;m1&#39;);
ylabel(&#39;n1&#39;);
title(&#39;greater than Nq&#39;);

ts2=0.01;
m2=0:5;
n2=2*sin(2*pi*m2*ts2/T);
subplot(2,2,3);
stem(m2,n2,&#39;b&#39;);
xlabel(&#39;m2&#39;);
ylabel(&#39;n2&#39;);
title(&#39;Equal to Nq&#39;);

ts3=0.1;
m3=0:15;
n3=2*sin(2*pi*m3*ts3/T);
subplot(2,2,4);
stem(m3,n3,&#39;b&#39;);
xlabel(&#39;m3&#39;);
ylabel(&#39;n3&#39;);
title(&#39;less than Nq&#39;);
