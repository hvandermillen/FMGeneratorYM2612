# FMGeneratorYM2612
A simple, object-oriented, four-operator FM synthesis sample generator based on the Yamaha YM2612 sound chip used in the Sega Genesis.

This project uses numpy, matplotlib.pyplot, soundfile, and IPython.display.

To run the program, you can simply click the "restart kernel and run all cells" button (the two forward arrows).

You can your own sounds in the last cell labeled "GENERATE SOUNDS HERE". To create your own sounds:
- Edit the constructors for each Operator or FeedbackOperator. The Operator constructor has 2 parameters: frequency and amplitude, while the FeedbackOperator has 3: frequency, amplitude, and feedback.
- Edit the ADSR for each Operator. Attack and decay are percentages of the duration of the signal; sustain is a value frmo 0 to 1; release is a percentage of the signal left over. For example, if you generate a 1 second signal with adsr (0.25,0.25,0.2,0.5), the signal will rise to amplitude 1 at 0.25 seconds, decay to amplitude 0.2 at 0.5 seconds, stay there for 0.25 seconds, and release to amplitude 0 over the last 0.25 seconds
- Choose how much the LFO will modulate each operator
- Choose the algorithm for your channel
- Generate an LFO(frequency, amplitude)
