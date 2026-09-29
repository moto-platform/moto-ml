# moto-ml

Part of [moto-platform](https://github.com/moto-platform), an SDV-style diagnostics, telemetry and rider-assistance platform for motorcycles (first vehicle: Honda CL250).

Offline model **training** (Python): context classification (first model: road type/surface/riding event), the combined anomaly model (early fusion: CAN + vibration + acoustic + thermal + context), rider identity/style/fatigue (Phase 2). Outputs are **exported** in the format appropriate for the target node: TFLite Micro or ESP-DL (for MCUs), ONNX/TFLite (for the Raspi).

**Status:** skeleton, no code yet. The build system, tests and CI are added by `/repo-bootstrap moto-ml` when work on this repo starts (setup order: `moto-vehicle-defs/docs/ARCHITECTURE.md` §9).

- Architecture and decisions: [moto-vehicle-defs/docs](https://github.com/moto-platform/moto-vehicle-defs/tree/main/docs) (`ARCHITECTURE.md`, `DECISIONS.md`)
- Signals, CAN IDs and DIDs come only from [moto-vehicle-defs](https://github.com/moto-platform/moto-vehicle-defs) (git submodule pinned to a tag)
- Scope rules for contributors and Claude Code: [`CLAUDE.md`](CLAUDE.md)

## License

MIT, see [LICENSE](LICENSE) (D-036).
