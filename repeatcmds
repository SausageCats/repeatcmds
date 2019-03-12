#!/bin/bash

_repeatcmds () {

  unset -f _repeatcmds

  if [ $# -lt 2 ]; then
    cat << EOF
usage: $(basename $0) <sleep[s]> <commands...>
EOF
    return 1
  fi

  local sec=$1
  shift

  while true; do
    for arg; do
      eval $arg
    done
    sleep $sec
  done

}

_repeatcmds "$@"
