
project(local_harfbuzz)

set(HARFBUZZ_SRC_DIR ${PROJECT_SOURCE_DIR}/../../../../thirdparty/${REPO_HARFBUZZ_SRCDIR})
set(HARFBUZZ_CONFIG_DIR ${PROJECT_SOURCE_DIR})

include_directories(${CMAKE_CURRENT_SOURCE_DIR})
include_directories(${HARFBUZZ_CONFIG_DIR})

add_definitions(-DHAVE_CONFIG_H=1)

set(HARFBUZZ_SRC_FILES
    ${HARFBUZZ_SRC_DIR}/src/hb-aat-layout.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-aat-map.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-blob.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-buffer.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-buffer-serialize.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-common.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-draw.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-face.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-fallback-shape.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-font.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-ft.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-map.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-number.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-ot-cff1-table.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-ot-cff2-table.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-ot-color.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-ot-face.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-ot-font.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-ot-layout.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-ot-map.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-ot-math.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-ot-meta.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-ot-metrics.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-ot-name.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-ot-shape-complex-arabic.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-ot-shape-complex-default.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-ot-shape-complex-hangul.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-ot-shape-complex-hebrew.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-ot-shape-complex-indic.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-ot-shape-complex-indic-table.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-ot-shape-complex-khmer.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-ot-shape-complex-myanmar.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-ot-shape-complex-syllabic.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-ot-shape-complex-thai.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-ot-shape-complex-use.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-ot-shape-complex-vowel-constraints.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-ot-shape-fallback.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-ot-shape-normalize.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-ot-shape.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-ot-tag.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-ot-var.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-set.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-shape.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-shape-plan.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-shaper.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-static.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-style.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-ucd.cc
    ${HARFBUZZ_SRC_DIR}/src/hb-unicode.cc
)

add_library(local_harfbuzz STATIC ${HARFBUZZ_SRC_FILES})
