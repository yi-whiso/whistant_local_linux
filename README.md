# Whistant Local AppImage Usage

## Download
- From GitHub Releases or provided distribution link.

## Run
```bash
chmod +x "Whistant Local-1.0.0.AppImage"
./Whistant\ Local-1.0.0.AppImage
```

## Configuration (optional)
- Defaults are built-in. To override:
  - User config file:
    ```bash
    mkdir -p ~/.whistant_local
    cat > ~/.whistant_local/.env << 'EOF'
    WHISTANT_SERVER_URL=https://whisolla.com:2087
    OLLAMA_SERVER_URL=http://localhost:11434
    EOF
    ```
  - Or place a `.env` next to the AppImage:
    ```bash
    cat > ./.env << 'EOF'
    WHISTANT_SERVER_URL=https://whisolla.com:2087
    OLLAMA_SERVER_URL=http://localhost:11434
    EOF
    ./Whistant\ Local-1.0.0.AppImage
    ```

## Requirements
- Node.js not required (bundled with Electron)
- Ollama running at `http://localhost:11434`
- Optional: `cloudflared` if remote access is needed.

## Data Location
- App data: `~/.config/Whistant Local`
- Optional config: `~/.whistant_local/.env`

## Verify
```bash
./Whistant\ Local-1.0.0.AppImage --version || echo "App launched"
ls -la ~/.config/Whistant\ Local
```
