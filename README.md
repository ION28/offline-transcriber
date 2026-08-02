# offline transscriber

```bash
npm install @huggingface/transformers onnxruntime-web
mkdir -p public/wasm
cp node_modules/onnxruntime-web/dist/*.wasm public/wasm/

npm run build
```

Obtaining whisper versions which go in public/models/Xenova/
```bash
apt install git-lfs -y

git lfs install

cd public/models/Xenova

git clone https://huggingface.co/Xenova/whisper-tiny
git clone https://huggingface.co/Xenova/whisper-base
git clone https://huggingface.co/Xenova/whisper-small

# Delete the .git histories to save space
rm -rf whisper-tiny/.git whisper-base/.git whisper-small/.git
```
