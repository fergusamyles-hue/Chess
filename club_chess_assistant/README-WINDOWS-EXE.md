# Build your Windows chess assistant EXE (no Python needed on your PC)

This package is configured to build `ClubChessAssistant.exe` on a hosted Windows runner.
You do **not** install Python or run commands on your own computer.

## One-time steps

1. Sign in to GitHub or create a free account at https://github.com.
2. Create a new repository. You can call it `club-chess-assistant`.
3. Choose **Add file → Upload files**.
4. Extract this ZIP on your PC, then upload the files and folders inside it to the repository.
   Make sure `.github/workflows/build.yml` is included. GitHub may hide `.github`; enable hidden files in File Explorer if needed.
5. Commit the upload.
6. Open the repository's **Actions** tab.
7. Select **Build Windows EXE** on the left, then **Run workflow**.
8. Wait for the run to finish successfully.
9. Open the completed run, scroll to **Artifacts**, and download `ClubChessAssistant-Windows`.
10. Extract that downloaded artifact. Double-click `ClubChessAssistant.exe`.

The resulting EXE is a portable, single-file Windows build. Windows SmartScreen may show a warning because it is an unsigned personal utility; only run the EXE you built from this source.

## What's in this prototype
- Custom minimax/alpha-beta chess search (not Stockfish).
- Clickable board, FEN import, undo and reset.
- Adjustable search depth and optional move noise.
- Screenshot reference viewer.

## Known limitations
- Automatic piece recognition from Chess.com screenshots is not included yet. The image viewer only displays the screenshot; enter the FEN to analyse the position.
- The ~1200 Elo rating is a tuning target, not a verified rating.
- Use for puzzles, offline practice and post-game analysis, not live online games.

## If GitHub doesn't show the workflow
Confirm `.github/workflows/build.yml` exists in the repository on its default branch. Then refresh the Actions tab.
