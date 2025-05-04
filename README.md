# CloneYourself
Create realistic deepfakes for UGC (User Generated Content) videos by cloning your voice and face.

## See it live and in action 📺
-  [🎥 Tutorial of Sesame CSM - Part 1 🇮🇹](URL_ADDRESS.be/SedGB8m2XLM) 
-  [🎥 Tutorial of FaceFusion - Part 2 🇮🇹](URL_ADDRESS.be/SedGB8m2XLM) 

[![Tutorial](https://imgur.com/mY2lLnO.png)](https://youtu.be/SedGB8m2XLM 'Tutorial')
<!-- <div style="display: flex; gap: 10px; align-items: center;">
  <a style="width: 50%; height: auto;" href="https://youtu.be/SedGB8m2XLM"><img src="https://imgur.com/mY2lLnO.png" alt="Image 1" ></a>
  <a style="width: 50%; height: auto;" href="https://youtu.be/SedGB8m2XLM"><img src="https://imgur.com/mY2lLnO.png" alt="Image 1" ></a>
</div> -->

# Startup 🚀
## 1. Sesame CSM Setup
1. Record at least 5 segment of your own voice saying 5 seconds sentences
2. Upload the 5 files audio to your drive.
3. <p>Upload the script [CSM_Custom.ipynb](CSM_Custom.ipynb) on <a href='https://colab.research.google.com/'> Google Colab </a> or &nbsp; <a target="_blank" href="https://colab.research.google.com/drive/14qGWyOiOEkfwmy5fzvNjvPUzb4gdI4LJ?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a></p>
4.  Change the runtime to GPU.
5. Create an <a href='https://huggingface.co/settings/tokens'>Hugging Face Token</a> and add the token to the Colab's Secrets with the name `hf` 
6. Change the `SPEAKER_PROMPTS` parameters in the `CSM_Custom.ipynb` notebook to match your own audio files and the respective transcriptions
7. Edit the `conversation` with the segments you want to be pronunced with your cloned voice.
8. Run the `CSM_Custom.ipynb` notebook.
9. Iterate until you get the desired results

## 2. FaceFusion Setup
1. Take a selfie  
2. Upload the selfie, your cloned voice and the Real UGC video with which you want to change your face on [Deepnote](https://deepnote.com)
3. Change the sources to your uploaded files in `!python facefusion.py headless-run --face-swapper-model ghost_2_256 -s data/selfie.jpeg -t data/UgcVideo.mp4 -o out/mytest1.mp4`, for face swapping and `!python facefusion.py headless-run --processors lip_syncer -s data/FinalClonedVoice.MP3 -t out/mytest1.mp4 -o out/final_output.mp4` for lip syncing.
4. Run the cells and wait for the process to complete.
5. Download the output video from the `out` folder.
<br>
<p>N.B. These instructions are for performing this procedure in the cloud and for free. Nothing prevents you from running them locally, but be careful to handle python enviroment properly and to adapt your configurations to conform to your system's requirements</a></p>

</br>

# Other References 🔗

<p>- <a href="https://github.com/SesameAILabs/csm">Sesame CSM (Conversational Speech Model)</a>: speech generation model from <a href='https://www.sesame.com/' >Sesame</a></p>
- <a href="https://github.com/facefusion/facefusion?tab=readme-ov-file">FaceFusion</a>: Industry leading face manipulation platform. <a href='https://docs.facefusion.io/'> Documentations </a> </p>

# Who, When, Why?

👨🏾‍💻 Author: Danilo Fiumi <br />
📅 Version: 1.x<br />
📜 License: This project is licensed under the MIT license. Feel free to use it, just don't do bad things with it.