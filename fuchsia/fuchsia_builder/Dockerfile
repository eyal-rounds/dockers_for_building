FROM eyalrounds/fuchsia_builder:latest
MAINTAINER eyalrounds
RUN bash -c "source scripts/env.sh && envprompt && fset x86-64 --no-goma --no-ccache && fbuild"
