run:
	@if ! command -v unshare >/dev/null; then \
		echo "SKIP others/odirect: unshare not available"; \
		exit 0; \
	fi; \
	if ! unshare -m --propagation slave true; then \
		echo "SKIP others/odirect: mount namespace not available"; \
		exit 0; \
	fi; \
	unshare -m --propagation slave ./run.sh

.PHONY: run
