# SPDX-License-Identifier: MIT

# This file was generated by
# scripts/copy_from_pqclean/copy_from_pqclean.py

if(OQS_ENABLE_KEM_kyber_512)
    add_library(kyber_512_clean OBJECT kem_kyber_512.c pqclean_kyber512_clean/cbd.c pqclean_kyber512_clean/indcpa.c pqclean_kyber512_clean/kem.c pqclean_kyber512_clean/ntt.c pqclean_kyber512_clean/poly.c pqclean_kyber512_clean/polyvec.c pqclean_kyber512_clean/reduce.c pqclean_kyber512_clean/symmetric-fips202.c pqclean_kyber512_clean/verify.c)
    target_include_directories(kyber_512_clean PRIVATE ${CMAKE_CURRENT_LIST_DIR}/pqclean_kyber512_clean)
    target_include_directories(kyber_512_clean PRIVATE ${PROJECT_SOURCE_DIR}/src/common/pqclean_shims)
    set(_KYBER_OBJS ${_KYBER_OBJS} $<TARGET_OBJECTS:kyber_512_clean>)
endif()

if(OQS_ENABLE_KEM_kyber_512_avx2)
    add_library(kyber_512_avx2 OBJECT pqclean_kyber512_avx2/basemul.S pqclean_kyber512_avx2/cbd.c pqclean_kyber512_avx2/consts.c pqclean_kyber512_avx2/fips202x4.c pqclean_kyber512_avx2/fq.s pqclean_kyber512_avx2/indcpa.c pqclean_kyber512_avx2/invntt.s pqclean_kyber512_avx2/kem.c pqclean_kyber512_avx2/ntt.s pqclean_kyber512_avx2/poly.c pqclean_kyber512_avx2/polyvec.c pqclean_kyber512_avx2/rejsample.c pqclean_kyber512_avx2/shuffle.s pqclean_kyber512_avx2/symmetric-fips202.c pqclean_kyber512_avx2/verify.c)
    target_include_directories(kyber_512_avx2 PRIVATE ${CMAKE_CURRENT_LIST_DIR}/pqclean_kyber512_avx2)
    target_include_directories(kyber_512_avx2 PRIVATE ${PROJECT_SOURCE_DIR}/src/common/pqclean_shims)
    target_compile_options(kyber_512_avx2 PRIVATE -mavx2 -mbmi2)
    set(_KYBER_OBJS ${_KYBER_OBJS} $<TARGET_OBJECTS:kyber_512_avx2>)
endif()

if(OQS_ENABLE_KEM_kyber_768)
    add_library(kyber_768_clean OBJECT kem_kyber_768.c pqclean_kyber768_clean/cbd.c pqclean_kyber768_clean/indcpa.c pqclean_kyber768_clean/kem.c pqclean_kyber768_clean/ntt.c pqclean_kyber768_clean/poly.c pqclean_kyber768_clean/polyvec.c pqclean_kyber768_clean/reduce.c pqclean_kyber768_clean/symmetric-fips202.c pqclean_kyber768_clean/verify.c)
    target_include_directories(kyber_768_clean PRIVATE ${CMAKE_CURRENT_LIST_DIR}/pqclean_kyber768_clean)
    target_include_directories(kyber_768_clean PRIVATE ${PROJECT_SOURCE_DIR}/src/common/pqclean_shims)
    set(_KYBER_OBJS ${_KYBER_OBJS} $<TARGET_OBJECTS:kyber_768_clean>)
endif()

if(OQS_ENABLE_KEM_kyber_768_avx2)
    add_library(kyber_768_avx2 OBJECT pqclean_kyber768_avx2/basemul.S pqclean_kyber768_avx2/cbd.c pqclean_kyber768_avx2/consts.c pqclean_kyber768_avx2/fips202x4.c pqclean_kyber768_avx2/fq.s pqclean_kyber768_avx2/indcpa.c pqclean_kyber768_avx2/invntt.s pqclean_kyber768_avx2/kem.c pqclean_kyber768_avx2/ntt.s pqclean_kyber768_avx2/poly.c pqclean_kyber768_avx2/polyvec.c pqclean_kyber768_avx2/rejsample.c pqclean_kyber768_avx2/shuffle.s pqclean_kyber768_avx2/symmetric-fips202.c pqclean_kyber768_avx2/verify.c)
    target_include_directories(kyber_768_avx2 PRIVATE ${CMAKE_CURRENT_LIST_DIR}/pqclean_kyber768_avx2)
    target_include_directories(kyber_768_avx2 PRIVATE ${PROJECT_SOURCE_DIR}/src/common/pqclean_shims)
    target_compile_options(kyber_768_avx2 PRIVATE -mavx2 -mbmi2 -mpopcnt)
    set(_KYBER_OBJS ${_KYBER_OBJS} $<TARGET_OBJECTS:kyber_768_avx2>)
endif()

if(OQS_ENABLE_KEM_kyber_1024)
    add_library(kyber_1024_clean OBJECT kem_kyber_1024.c pqclean_kyber1024_clean/cbd.c pqclean_kyber1024_clean/indcpa.c pqclean_kyber1024_clean/kem.c pqclean_kyber1024_clean/ntt.c pqclean_kyber1024_clean/poly.c pqclean_kyber1024_clean/polyvec.c pqclean_kyber1024_clean/reduce.c pqclean_kyber1024_clean/symmetric-fips202.c pqclean_kyber1024_clean/verify.c)
    target_include_directories(kyber_1024_clean PRIVATE ${CMAKE_CURRENT_LIST_DIR}/pqclean_kyber1024_clean)
    target_include_directories(kyber_1024_clean PRIVATE ${PROJECT_SOURCE_DIR}/src/common/pqclean_shims)
    set(_KYBER_OBJS ${_KYBER_OBJS} $<TARGET_OBJECTS:kyber_1024_clean>)
endif()

if(OQS_ENABLE_KEM_kyber_1024_avx2)
    add_library(kyber_1024_avx2 OBJECT pqclean_kyber1024_avx2/basemul.S pqclean_kyber1024_avx2/cbd.c pqclean_kyber1024_avx2/consts.c pqclean_kyber1024_avx2/fips202x4.c pqclean_kyber1024_avx2/fq.s pqclean_kyber1024_avx2/indcpa.c pqclean_kyber1024_avx2/invntt.s pqclean_kyber1024_avx2/kem.c pqclean_kyber1024_avx2/ntt.s pqclean_kyber1024_avx2/poly.c pqclean_kyber1024_avx2/polyvec.c pqclean_kyber1024_avx2/rejsample.c pqclean_kyber1024_avx2/shuffle.s pqclean_kyber1024_avx2/symmetric-fips202.c pqclean_kyber1024_avx2/verify.c)
    target_include_directories(kyber_1024_avx2 PRIVATE ${CMAKE_CURRENT_LIST_DIR}/pqclean_kyber1024_avx2)
    target_include_directories(kyber_1024_avx2 PRIVATE ${PROJECT_SOURCE_DIR}/src/common/pqclean_shims)
    target_compile_options(kyber_1024_avx2 PRIVATE -mavx2 -mbmi2 -mpopcnt)
    set(_KYBER_OBJS ${_KYBER_OBJS} $<TARGET_OBJECTS:kyber_1024_avx2>)
endif()

if(OQS_ENABLE_KEM_kyber_512_90s)
    add_library(kyber_512_90s_clean OBJECT kem_kyber_512_90s.c pqclean_kyber512-90s_clean/aes256ctr.c pqclean_kyber512-90s_clean/cbd.c pqclean_kyber512-90s_clean/indcpa.c pqclean_kyber512-90s_clean/kem.c pqclean_kyber512-90s_clean/ntt.c pqclean_kyber512-90s_clean/poly.c pqclean_kyber512-90s_clean/polyvec.c pqclean_kyber512-90s_clean/reduce.c pqclean_kyber512-90s_clean/verify.c)
    target_include_directories(kyber_512_90s_clean PRIVATE ${CMAKE_CURRENT_LIST_DIR}/pqclean_kyber512-90s_clean)
    target_include_directories(kyber_512_90s_clean PRIVATE ${PROJECT_SOURCE_DIR}/src/common/pqclean_shims)
    set(_KYBER_OBJS ${_KYBER_OBJS} $<TARGET_OBJECTS:kyber_512_90s_clean>)
endif()

if(OQS_ENABLE_KEM_kyber_512_90s_avx2)
    add_library(kyber_512_90s_avx2 OBJECT pqclean_kyber512-90s_avx2/aes256ctr.c pqclean_kyber512-90s_avx2/basemul.S pqclean_kyber512-90s_avx2/cbd.c pqclean_kyber512-90s_avx2/consts.c pqclean_kyber512-90s_avx2/fq.s pqclean_kyber512-90s_avx2/indcpa.c pqclean_kyber512-90s_avx2/invntt.s pqclean_kyber512-90s_avx2/kem.c pqclean_kyber512-90s_avx2/ntt.s pqclean_kyber512-90s_avx2/poly.c pqclean_kyber512-90s_avx2/polyvec.c pqclean_kyber512-90s_avx2/rejsample.c pqclean_kyber512-90s_avx2/shuffle.s pqclean_kyber512-90s_avx2/verify.c)
    target_include_directories(kyber_512_90s_avx2 PRIVATE ${CMAKE_CURRENT_LIST_DIR}/pqclean_kyber512-90s_avx2)
    target_include_directories(kyber_512_90s_avx2 PRIVATE ${PROJECT_SOURCE_DIR}/src/common/pqclean_shims)
    target_compile_options(kyber_512_90s_avx2 PRIVATE -maes -mavx2 -mbmi2 -mpopcnt)
    set(_KYBER_OBJS ${_KYBER_OBJS} $<TARGET_OBJECTS:kyber_512_90s_avx2>)
endif()

if(OQS_ENABLE_KEM_kyber_768_90s)
    add_library(kyber_768_90s_clean OBJECT kem_kyber_768_90s.c pqclean_kyber768-90s_clean/aes256ctr.c pqclean_kyber768-90s_clean/cbd.c pqclean_kyber768-90s_clean/indcpa.c pqclean_kyber768-90s_clean/kem.c pqclean_kyber768-90s_clean/ntt.c pqclean_kyber768-90s_clean/poly.c pqclean_kyber768-90s_clean/polyvec.c pqclean_kyber768-90s_clean/reduce.c pqclean_kyber768-90s_clean/verify.c)
    target_include_directories(kyber_768_90s_clean PRIVATE ${CMAKE_CURRENT_LIST_DIR}/pqclean_kyber768-90s_clean)
    target_include_directories(kyber_768_90s_clean PRIVATE ${PROJECT_SOURCE_DIR}/src/common/pqclean_shims)
    set(_KYBER_OBJS ${_KYBER_OBJS} $<TARGET_OBJECTS:kyber_768_90s_clean>)
endif()

if(OQS_ENABLE_KEM_kyber_768_90s_avx2)
    add_library(kyber_768_90s_avx2 OBJECT pqclean_kyber768-90s_avx2/aes256ctr.c pqclean_kyber768-90s_avx2/basemul.S pqclean_kyber768-90s_avx2/cbd.c pqclean_kyber768-90s_avx2/consts.c pqclean_kyber768-90s_avx2/fq.s pqclean_kyber768-90s_avx2/indcpa.c pqclean_kyber768-90s_avx2/invntt.s pqclean_kyber768-90s_avx2/kem.c pqclean_kyber768-90s_avx2/ntt.s pqclean_kyber768-90s_avx2/poly.c pqclean_kyber768-90s_avx2/polyvec.c pqclean_kyber768-90s_avx2/rejsample.c pqclean_kyber768-90s_avx2/shuffle.s pqclean_kyber768-90s_avx2/verify.c)
    target_include_directories(kyber_768_90s_avx2 PRIVATE ${CMAKE_CURRENT_LIST_DIR}/pqclean_kyber768-90s_avx2)
    target_include_directories(kyber_768_90s_avx2 PRIVATE ${PROJECT_SOURCE_DIR}/src/common/pqclean_shims)
    target_compile_options(kyber_768_90s_avx2 PRIVATE -maes -mavx2 -mbmi2 -mpopcnt)
    set(_KYBER_OBJS ${_KYBER_OBJS} $<TARGET_OBJECTS:kyber_768_90s_avx2>)
endif()

if(OQS_ENABLE_KEM_kyber_1024_90s)
    add_library(kyber_1024_90s_clean OBJECT kem_kyber_1024_90s.c pqclean_kyber1024-90s_clean/aes256ctr.c pqclean_kyber1024-90s_clean/cbd.c pqclean_kyber1024-90s_clean/indcpa.c pqclean_kyber1024-90s_clean/kem.c pqclean_kyber1024-90s_clean/ntt.c pqclean_kyber1024-90s_clean/poly.c pqclean_kyber1024-90s_clean/polyvec.c pqclean_kyber1024-90s_clean/reduce.c pqclean_kyber1024-90s_clean/verify.c)
    target_include_directories(kyber_1024_90s_clean PRIVATE ${CMAKE_CURRENT_LIST_DIR}/pqclean_kyber1024-90s_clean)
    target_include_directories(kyber_1024_90s_clean PRIVATE ${PROJECT_SOURCE_DIR}/src/common/pqclean_shims)
    set(_KYBER_OBJS ${_KYBER_OBJS} $<TARGET_OBJECTS:kyber_1024_90s_clean>)
endif()

if(OQS_ENABLE_KEM_kyber_1024_90s_avx2)
    add_library(kyber_1024_90s_avx2 OBJECT pqclean_kyber1024-90s_avx2/aes256ctr.c pqclean_kyber1024-90s_avx2/basemul.S pqclean_kyber1024-90s_avx2/cbd.c pqclean_kyber1024-90s_avx2/consts.c pqclean_kyber1024-90s_avx2/fq.s pqclean_kyber1024-90s_avx2/indcpa.c pqclean_kyber1024-90s_avx2/invntt.s pqclean_kyber1024-90s_avx2/kem.c pqclean_kyber1024-90s_avx2/ntt.s pqclean_kyber1024-90s_avx2/poly.c pqclean_kyber1024-90s_avx2/polyvec.c pqclean_kyber1024-90s_avx2/rejsample.c pqclean_kyber1024-90s_avx2/shuffle.s pqclean_kyber1024-90s_avx2/verify.c)
    target_include_directories(kyber_1024_90s_avx2 PRIVATE ${CMAKE_CURRENT_LIST_DIR}/pqclean_kyber1024-90s_avx2)
    target_include_directories(kyber_1024_90s_avx2 PRIVATE ${PROJECT_SOURCE_DIR}/src/common/pqclean_shims)
    target_compile_options(kyber_1024_90s_avx2 PRIVATE -maes -mavx2 -mbmi2 -mpopcnt)
    set(_KYBER_OBJS ${_KYBER_OBJS} $<TARGET_OBJECTS:kyber_1024_90s_avx2>)
endif()

set(KYBER_OBJS ${_KYBER_OBJS} PARENT_SCOPE)
