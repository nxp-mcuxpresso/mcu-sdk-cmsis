#
# Copyright 2024 NXP
#
# SPDX-License-Identifier: Apache-2.0
#

if (CONFIG_MCUX_COMPONENT_CMSIS_Include_core_cm)
    mcux_add_source(
        SOURCES Core/Include/cmsis_armclang.h
        SOURCES Core/Include/m-profile/cmsis_armclang_m.h
        COMPILERS armclang
    )

    mcux_add_source(
        SOURCES Core/Include/cmsis_compiler.h
        SOURCES Core/Include/cmsis_version.h
        COMPILERS armclang armcc gcc iar
    )

    mcux_add_source(
        SOURCES Core/Include/m-profile/cmsis_iccarm_m.h
        COMPILERS iar
    )

    mcux_add_source(
        SOURCES Core/Include/cmsis_gcc.h
        SOURCES Core/Include/m-profile/cmsis_gcc_m.h
        COMPILERS gcc
    )

    mcux_add_source(
        SOURCES Core/Include/core_cm0.h
        CORES cm0
    )

    mcux_add_source(
        SOURCES Core/Include/core_cm0plus.h
        CORES cm0p
    )

    mcux_add_source(
        SOURCES Core/Include/core_cm23.h
        CORES cm23
    )

    mcux_add_source(
        SOURCES Core/Include/core_cm3.h
        CORES cm3
    )

    mcux_add_source(
        SOURCES Core/Include/core_cm33.h
        CORES cm33 cm33f
    )

    mcux_add_source(
        SOURCES Core/Include/core_cm4.h
        CORES cm4 cm4f
    )

    mcux_add_source(
        SOURCES Core/Include/core_cm7.h
        SOURCES Core/Include/m-profile/armv7m_cachel1.h
        CORES cm7 cm7f
    )

    mcux_add_source(
        SOURCES Core/Include/m-profile/armv7m_mpu.h
        CORES cm0 cm0p cm3 cm4 cm4f cm7 cm7f
    )

    mcux_add_source(
        SOURCES Core/Include/m-profile/armv8m_mpu.h
        SOURCES Core/Include/tz_context.h
        CORES cm23 cm33 cm33f
    )

    mcux_add_include(
        INCLUDES
            Core/Include/./
            Core/Include/m-profile/./
    )

endif()

if (CONFIG_MCUX_COMPONENT_CMSIS_Include_core_ca7)
    mcux_add_source(
        SOURCES CMSIS/Include/cmsis_compiler.h
        SOURCES CMSIS/Include/a-profile/cmsis_cp15.h
        SOURCES CMSIS/Include/a-profile/irq_ctrl.h
        SOURCES CMSIS/Source/irq_ctrl_gic.c
        COMPILERS armclang armcc gcc iar
    )

    mcux_add_source(
        SOURCES CMSIS/Include/core_ca.h
        CORES ca7
    )

    mcux_add_source(
        SOURCES CMSIS/Include/a-profile/cmsis_armclang_a.h
        COMPILERS armclang
    )

    mcux_add_source(
        SOURCES Core/Include/cmsis_gcc.h
        SOURCES CMSIS/Include/a-profile/cmsis_gcc_a.h
        COMPILERS gcc
    )

    mcux_add_source(
        SOURCES CMSIS/Include/a-profile/cmsis_iccarm_a.h
        COMPILERS iar
    )

    mcux_add_include(
        INCLUDES
            Core/Include/./
            Core/Include/a-profile/./
    )

endif()

if (CONFIG_MCUX_COMPONENT_CMSIS_DSP_Include)
    mcux_add_source(
        SOURCES
            DSP/Include/arm_common_tables.h
            DSP/Include/arm_common_tables_f16.h
            DSP/Include/arm_const_structs.h
            DSP/Include/arm_const_structs_f16.h
            DSP/Include/arm_helium_utils.h
            DSP/Include/arm_math.h
            DSP/Include/arm_math_f16.h
            DSP/Include/arm_math_memory.h
            DSP/Include/arm_math_types.h
            DSP/Include/arm_math_types_f16.h
            DSP/Include/arm_mve_tables.h
            DSP/Include/arm_mve_tables_f16.h
            DSP/Include/arm_vec_math.h
            DSP/Include/arm_vec_math_f16.h
            DSP/Include/dsp/basic_math_functions.h
            DSP/Include/dsp/basic_math_functions_f16.h
            DSP/Include/dsp/bayes_functions.h
            DSP/Include/dsp/bayes_functions_f16.h
            DSP/Include/dsp/complex_math_functions.h
            DSP/Include/dsp/complex_math_functions_f16.h
            DSP/Include/dsp/controller_functions.h
            DSP/Include/dsp/controller_functions_f16.h
            DSP/Include/dsp/debug.h
            DSP/Include/dsp/distance_functions.h
            DSP/Include/dsp/distance_functions_f16.h
            DSP/Include/dsp/fast_math_functions.h
            DSP/Include/dsp/fast_math_functions_f16.h
            DSP/Include/dsp/filtering_functions.h
            DSP/Include/dsp/filtering_functions_f16.h
            DSP/Include/dsp/interpolation_functions.h
            DSP/Include/dsp/interpolation_functions_f16.h
            DSP/Include/dsp/matrix_functions.h
            DSP/Include/dsp/matrix_functions_f16.h
            DSP/Include/dsp/matrix_utils.h
            DSP/Include/dsp/none.h
            DSP/Include/dsp/quaternion_math_functions.h
            DSP/Include/dsp/statistics_functions.h
            DSP/Include/dsp/statistics_functions_f16.h
            DSP/Include/dsp/support_functions.h
            DSP/Include/dsp/support_functions_f16.h
            DSP/Include/dsp/svm_defines.h
            DSP/Include/dsp/svm_functions.h
            DSP/Include/dsp/svm_functions_f16.h
            DSP/Include/dsp/transform_functions.h
            DSP/Include/dsp/transform_functions_f16.h
            DSP/Include/dsp/utils.h
            DSP/Include/dsp/window_functions.h
            DSP/PrivateInclude/arm_sorting.h
            DSP/PrivateInclude/arm_vec_fft.h
            DSP/PrivateInclude/arm_vec_filtering.h
    )

    mcux_add_include(
        INCLUDES
            DSP/Include
            DSP/PrivateInclude
    )

endif()

if (CONFIG_MCUX_COMPONENT_CMSIS_DSP_Source)
    mcux_add_source(
        SOURCES
            DSP/Include/arm_common_tables.h
            DSP/Include/arm_common_tables_f16.h
            DSP/Include/arm_const_structs.h
            DSP/Include/arm_const_structs_f16.h
            DSP/Include/arm_helium_utils.h
            DSP/Include/arm_math.h
            DSP/Include/arm_math_f16.h
            DSP/Include/arm_math_memory.h
            DSP/Include/arm_math_types.h
            DSP/Include/arm_math_types_f16.h
            DSP/Include/arm_mve_tables.h
            DSP/Include/arm_mve_tables_f16.h
            DSP/Include/arm_vec_math.h
            DSP/Include/arm_vec_math_f16.h
            DSP/Include/dsp/basic_math_functions.h
            DSP/Include/dsp/basic_math_functions_f16.h
            DSP/Include/dsp/bayes_functions.h
            DSP/Include/dsp/bayes_functions_f16.h
            DSP/Include/dsp/complex_math_functions.h
            DSP/Include/dsp/complex_math_functions_f16.h
            DSP/Include/dsp/controller_functions.h
            DSP/Include/dsp/controller_functions_f16.h
            DSP/Include/dsp/debug.h
            DSP/Include/dsp/distance_functions.h
            DSP/Include/dsp/distance_functions_f16.h
            DSP/Include/dsp/fast_math_functions.h
            DSP/Include/dsp/fast_math_functions_f16.h
            DSP/Include/dsp/filtering_functions.h
            DSP/Include/dsp/filtering_functions_f16.h
            DSP/Include/dsp/interpolation_functions.h
            DSP/Include/dsp/interpolation_functions_f16.h
            DSP/Include/dsp/matrix_functions.h
            DSP/Include/dsp/matrix_functions_f16.h
            DSP/Include/dsp/matrix_utils.h
            DSP/Include/dsp/none.h
            DSP/Include/dsp/quaternion_math_functions.h
            DSP/Include/dsp/statistics_functions.h
            DSP/Include/dsp/statistics_functions_f16.h
            DSP/Include/dsp/support_functions.h
            DSP/Include/dsp/support_functions_f16.h
            DSP/Include/dsp/svm_defines.h
            DSP/Include/dsp/svm_functions.h
            DSP/Include/dsp/svm_functions_f16.h
            DSP/Include/dsp/transform_functions.h
            DSP/Include/dsp/transform_functions_f16.h
            DSP/Include/dsp/utils.h
            DSP/Include/dsp/window_functions.h
            DSP/PrivateInclude/arm_sorting.h
            DSP/PrivateInclude/arm_vec_fft.h
            DSP/PrivateInclude/arm_vec_filtering.h
            DSP/Source/BasicMathFunctions/BasicMathFunctions.c
            DSP/Source/BasicMathFunctions/BasicMathFunctionsF16.c
            DSP/Source/BayesFunctions/BayesFunctions.c
            DSP/Source/BayesFunctions/BayesFunctionsF16.c
            DSP/Source/CommonTables/CommonTables.c
            DSP/Source/CommonTables/CommonTablesF16.c
            DSP/Source/ComplexMathFunctions/ComplexMathFunctions.c
            DSP/Source/ComplexMathFunctions/ComplexMathFunctionsF16.c
            DSP/Source/ControllerFunctions/ControllerFunctions.c
            DSP/Source/DistanceFunctions/DistanceFunctions.c
            DSP/Source/DistanceFunctions/arm_boolean_distance_template.h
            DSP/Source/DistanceFunctions/DistanceFunctionsF16.c
            DSP/Source/FastMathFunctions/FastMathFunctions.c
            DSP/Source/FastMathFunctions/FastMathFunctionsF16.c
            DSP/Source/FilteringFunctions/FilteringFunctions.c
            DSP/Source/FilteringFunctions/FilteringFunctionsF16.c
            DSP/Source/InterpolationFunctions/InterpolationFunctions.c
            DSP/Source/InterpolationFunctions/InterpolationFunctionsF16.c
            DSP/Source/MatrixFunctions/MatrixFunctions.c
            DSP/Source/MatrixFunctions/MatrixFunctionsF16.c
            DSP/Source/QuaternionMathFunctions/QuaternionMathFunctions.c
            DSP/Source/SVMFunctions/SVMFunctions.c
            DSP/Source/SVMFunctions/SVMFunctionsF16.c
            DSP/Source/StatisticsFunctions/StatisticsFunctions.c
            DSP/Source/StatisticsFunctions/StatisticsFunctionsF16.c
            DSP/Source/SupportFunctions/SupportFunctions.c
            DSP/Source/SupportFunctions/SupportFunctionsF16.c
            DSP/Source/TransformFunctions/TransformFunctions.c
            DSP/Source/TransformFunctions/TransformFunctionsF16.c
            DSP/Source/WindowFunctions/WindowFunctions.c
    )

    mcux_add_source(
        EXCLUDE TRUE
        SOURCES
            DSP/Source/BasicMathFunctions/arm_abs_f32.c
            DSP/Source/BasicMathFunctions/arm_abs_f64.c
            DSP/Source/BasicMathFunctions/arm_abs_q15.c
            DSP/Source/BasicMathFunctions/arm_abs_q31.c
            DSP/Source/BasicMathFunctions/arm_abs_q7.c
            DSP/Source/BasicMathFunctions/arm_add_f32.c
            DSP/Source/BasicMathFunctions/arm_add_f64.c
            DSP/Source/BasicMathFunctions/arm_add_q15.c
            DSP/Source/BasicMathFunctions/arm_add_q31.c
            DSP/Source/BasicMathFunctions/arm_add_q7.c
            DSP/Source/BasicMathFunctions/arm_and_u16.c
            DSP/Source/BasicMathFunctions/arm_and_u32.c
            DSP/Source/BasicMathFunctions/arm_and_u8.c
            DSP/Source/BasicMathFunctions/arm_clip_f32.c
            DSP/Source/BasicMathFunctions/arm_clip_q15.c
            DSP/Source/BasicMathFunctions/arm_clip_q31.c
            DSP/Source/BasicMathFunctions/arm_clip_q7.c
            DSP/Source/BasicMathFunctions/arm_dot_prod_f32.c
            DSP/Source/BasicMathFunctions/arm_dot_prod_f64.c
            DSP/Source/BasicMathFunctions/arm_dot_prod_q15.c
            DSP/Source/BasicMathFunctions/arm_dot_prod_q31.c
            DSP/Source/BasicMathFunctions/arm_dot_prod_q7.c
            DSP/Source/BasicMathFunctions/arm_mult_f32.c
            DSP/Source/BasicMathFunctions/arm_mult_f64.c
            DSP/Source/BasicMathFunctions/arm_mult_q15.c
            DSP/Source/BasicMathFunctions/arm_mult_q31.c
            DSP/Source/BasicMathFunctions/arm_mult_q7.c
            DSP/Source/BasicMathFunctions/arm_negate_f32.c
            DSP/Source/BasicMathFunctions/arm_negate_f64.c
            DSP/Source/BasicMathFunctions/arm_negate_q15.c
            DSP/Source/BasicMathFunctions/arm_negate_q31.c
            DSP/Source/BasicMathFunctions/arm_negate_q7.c
            DSP/Source/BasicMathFunctions/arm_not_u16.c
            DSP/Source/BasicMathFunctions/arm_not_u32.c
            DSP/Source/BasicMathFunctions/arm_not_u8.c
            DSP/Source/BasicMathFunctions/arm_offset_f32.c
            DSP/Source/BasicMathFunctions/arm_offset_f64.c
            DSP/Source/BasicMathFunctions/arm_offset_q15.c
            DSP/Source/BasicMathFunctions/arm_offset_q31.c
            DSP/Source/BasicMathFunctions/arm_offset_q7.c
            DSP/Source/BasicMathFunctions/arm_or_u16.c
            DSP/Source/BasicMathFunctions/arm_or_u32.c
            DSP/Source/BasicMathFunctions/arm_or_u8.c
            DSP/Source/BasicMathFunctions/arm_scale_f32.c
            DSP/Source/BasicMathFunctions/arm_scale_f64.c
            DSP/Source/BasicMathFunctions/arm_scale_q15.c
            DSP/Source/BasicMathFunctions/arm_scale_q31.c
            DSP/Source/BasicMathFunctions/arm_scale_q7.c
            DSP/Source/BasicMathFunctions/arm_shift_q15.c
            DSP/Source/BasicMathFunctions/arm_shift_q31.c
            DSP/Source/BasicMathFunctions/arm_shift_q7.c
            DSP/Source/BasicMathFunctions/arm_sub_f32.c
            DSP/Source/BasicMathFunctions/arm_sub_f64.c
            DSP/Source/BasicMathFunctions/arm_sub_q15.c
            DSP/Source/BasicMathFunctions/arm_sub_q31.c
            DSP/Source/BasicMathFunctions/arm_sub_q7.c
            DSP/Source/BasicMathFunctions/arm_xor_u16.c
            DSP/Source/BasicMathFunctions/arm_xor_u32.c
            DSP/Source/BasicMathFunctions/arm_xor_u8.c
            DSP/Source/BasicMathFunctions/arm_abs_f16.c
            DSP/Source/BasicMathFunctions/arm_add_f16.c
            DSP/Source/BasicMathFunctions/arm_clip_f16.c
            DSP/Source/BasicMathFunctions/arm_dot_prod_f16.c
            DSP/Source/BasicMathFunctions/arm_mult_f16.c
            DSP/Source/BasicMathFunctions/arm_negate_f16.c
            DSP/Source/BasicMathFunctions/arm_offset_f16.c
            DSP/Source/BasicMathFunctions/arm_scale_f16.c
            DSP/Source/BasicMathFunctions/arm_sub_f16.c
            DSP/Source/BayesFunctions/arm_gaussian_naive_bayes_predict_f32.c
            DSP/Source/BayesFunctions/arm_gaussian_naive_bayes_predict_f16.c
            DSP/Source/CommonTables/arm_common_tables.c
            DSP/Source/CommonTables/arm_const_structs.c
            DSP/Source/CommonTables/arm_mve_tables.c
            DSP/Source/CommonTables/arm_common_tables_f16.c
            DSP/Source/CommonTables/arm_const_structs_f16.c
            DSP/Source/CommonTables/arm_mve_tables_f16.c
            DSP/Source/ComplexMathFunctions/arm_cmplx_conj_f32.c
            DSP/Source/ComplexMathFunctions/arm_cmplx_conj_q15.c
            DSP/Source/ComplexMathFunctions/arm_cmplx_conj_q31.c
            DSP/Source/ComplexMathFunctions/arm_cmplx_dot_prod_f32.c
            DSP/Source/ComplexMathFunctions/arm_cmplx_dot_prod_q15.c
            DSP/Source/ComplexMathFunctions/arm_cmplx_dot_prod_q31.c
            DSP/Source/ComplexMathFunctions/arm_cmplx_mag_f32.c
            DSP/Source/ComplexMathFunctions/arm_cmplx_mag_f64.c
            DSP/Source/ComplexMathFunctions/arm_cmplx_mag_fast_q15.c
            DSP/Source/ComplexMathFunctions/arm_cmplx_mag_q15.c
            DSP/Source/ComplexMathFunctions/arm_cmplx_mag_q31.c
            DSP/Source/ComplexMathFunctions/arm_cmplx_mag_squared_f32.c
            DSP/Source/ComplexMathFunctions/arm_cmplx_mag_squared_f64.c
            DSP/Source/ComplexMathFunctions/arm_cmplx_mag_squared_q15.c
            DSP/Source/ComplexMathFunctions/arm_cmplx_mag_squared_q31.c
            DSP/Source/ComplexMathFunctions/arm_cmplx_mult_cmplx_f32.c
            DSP/Source/ComplexMathFunctions/arm_cmplx_mult_cmplx_f64.c
            DSP/Source/ComplexMathFunctions/arm_cmplx_mult_cmplx_q15.c
            DSP/Source/ComplexMathFunctions/arm_cmplx_mult_cmplx_q31.c
            DSP/Source/ComplexMathFunctions/arm_cmplx_mult_real_f32.c
            DSP/Source/ComplexMathFunctions/arm_cmplx_mult_real_q15.c
            DSP/Source/ComplexMathFunctions/arm_cmplx_mult_real_q31.c
            DSP/Source/ComplexMathFunctions/arm_cmplx_conj_f16.c
            DSP/Source/ComplexMathFunctions/arm_cmplx_dot_prod_f16.c
            DSP/Source/ComplexMathFunctions/arm_cmplx_mag_f16.c
            DSP/Source/ComplexMathFunctions/arm_cmplx_mag_squared_f16.c
            DSP/Source/ComplexMathFunctions/arm_cmplx_mult_cmplx_f16.c
            DSP/Source/ComplexMathFunctions/arm_cmplx_mult_real_f16.c
            DSP/Source/ControllerFunctions/arm_pid_init_f32.c
            DSP/Source/ControllerFunctions/arm_pid_init_q15.c
            DSP/Source/ControllerFunctions/arm_pid_init_q31.c
            DSP/Source/ControllerFunctions/arm_pid_reset_f32.c
            DSP/Source/ControllerFunctions/arm_pid_reset_q15.c
            DSP/Source/ControllerFunctions/arm_pid_reset_q31.c
            DSP/Source/ControllerFunctions/arm_sin_cos_f32.c
            DSP/Source/ControllerFunctions/arm_sin_cos_q31.c
            DSP/Source/DistanceFunctions/arm_boolean_distance.c
            DSP/Source/DistanceFunctions/arm_braycurtis_distance_f32.c
            DSP/Source/DistanceFunctions/arm_canberra_distance_f32.c
            DSP/Source/DistanceFunctions/arm_chebyshev_distance_f32.c
            DSP/Source/DistanceFunctions/arm_chebyshev_distance_f64.c
            DSP/Source/DistanceFunctions/arm_cityblock_distance_f32.c
            DSP/Source/DistanceFunctions/arm_cityblock_distance_f64.c
            DSP/Source/DistanceFunctions/arm_correlation_distance_f32.c
            DSP/Source/DistanceFunctions/arm_cosine_distance_f32.c
            DSP/Source/DistanceFunctions/arm_cosine_distance_f64.c
            DSP/Source/DistanceFunctions/arm_dice_distance.c
            DSP/Source/DistanceFunctions/arm_dtw_distance_f32.c
            DSP/Source/DistanceFunctions/arm_dtw_init_window_q7.c
            DSP/Source/DistanceFunctions/arm_dtw_path_f32.c
            DSP/Source/DistanceFunctions/arm_euclidean_distance_f32.c
            DSP/Source/DistanceFunctions/arm_euclidean_distance_f64.c
            DSP/Source/DistanceFunctions/arm_hamming_distance.c
            DSP/Source/DistanceFunctions/arm_jaccard_distance.c
            DSP/Source/DistanceFunctions/arm_jensenshannon_distance_f32.c
            DSP/Source/DistanceFunctions/arm_kulsinski_distance.c
            DSP/Source/DistanceFunctions/arm_minkowski_distance_f32.c
            DSP/Source/DistanceFunctions/arm_rogerstanimoto_distance.c
            DSP/Source/DistanceFunctions/arm_russellrao_distance.c
            DSP/Source/DistanceFunctions/arm_sokalmichener_distance.c
            DSP/Source/DistanceFunctions/arm_sokalsneath_distance.c
            DSP/Source/DistanceFunctions/arm_yule_distance.c
            DSP/Source/DistanceFunctions/arm_braycurtis_distance_f16.c
            DSP/Source/DistanceFunctions/arm_chebyshev_distance_f16.c
            DSP/Source/DistanceFunctions/arm_canberra_distance_f16.c
            DSP/Source/DistanceFunctions/arm_cityblock_distance_f16.c
            DSP/Source/DistanceFunctions/arm_correlation_distance_f16.c
            DSP/Source/DistanceFunctions/arm_cosine_distance_f16.c
            DSP/Source/DistanceFunctions/arm_euclidean_distance_f16.c
            DSP/Source/DistanceFunctions/arm_jensenshannon_distance_f16.c
            DSP/Source/DistanceFunctions/arm_minkowski_distance_f16.c
            DSP/Source/FastMathFunctions/arm_atan2_f32.c
            DSP/Source/FastMathFunctions/arm_atan2_q15.c
            DSP/Source/FastMathFunctions/arm_atan2_q31.c
            DSP/Source/FastMathFunctions/arm_cos_f32.c
            DSP/Source/FastMathFunctions/arm_cos_q15.c
            DSP/Source/FastMathFunctions/arm_cos_q31.c
            DSP/Source/FastMathFunctions/arm_divide_q15.c
            DSP/Source/FastMathFunctions/arm_divide_q31.c
            DSP/Source/FastMathFunctions/arm_sin_f32.c
            DSP/Source/FastMathFunctions/arm_sin_q15.c
            DSP/Source/FastMathFunctions/arm_sin_q31.c
            DSP/Source/FastMathFunctions/arm_sqrt_q15.c
            DSP/Source/FastMathFunctions/arm_sqrt_q31.c
            DSP/Source/FastMathFunctions/arm_vexp_f32.c
            DSP/Source/FastMathFunctions/arm_vexp_f64.c
            DSP/Source/FastMathFunctions/arm_vlog_f32.c
            DSP/Source/FastMathFunctions/arm_vlog_f64.c
            DSP/Source/FastMathFunctions/arm_vlog_q15.c
            DSP/Source/FastMathFunctions/arm_vlog_q31.c
            DSP/Source/FastMathFunctions/arm_atan2_f16.c
            DSP/Source/FastMathFunctions/arm_vexp_f16.c
            DSP/Source/FastMathFunctions/arm_vinverse_f16.c
            DSP/Source/FastMathFunctions/arm_vlog_f16.c
            DSP/Source/FilteringFunctions/arm_biquad_cascade_df1_32x64_init_q31.c
            DSP/Source/FilteringFunctions/arm_biquad_cascade_df1_32x64_q31.c
            DSP/Source/FilteringFunctions/arm_biquad_cascade_df1_f32.c
            DSP/Source/FilteringFunctions/arm_biquad_cascade_df1_fast_q15.c
            DSP/Source/FilteringFunctions/arm_biquad_cascade_df1_fast_q31.c
            DSP/Source/FilteringFunctions/arm_biquad_cascade_df1_init_f32.c
            DSP/Source/FilteringFunctions/arm_biquad_cascade_df1_init_q15.c
            DSP/Source/FilteringFunctions/arm_biquad_cascade_df1_init_q31.c
            DSP/Source/FilteringFunctions/arm_biquad_cascade_df1_q15.c
            DSP/Source/FilteringFunctions/arm_biquad_cascade_df1_q31.c
            DSP/Source/FilteringFunctions/arm_biquad_cascade_df2T_f32.c
            DSP/Source/FilteringFunctions/arm_biquad_cascade_df2T_f64.c
            DSP/Source/FilteringFunctions/arm_biquad_cascade_df2T_init_f32.c
            DSP/Source/FilteringFunctions/arm_biquad_cascade_df2T_init_f64.c
            DSP/Source/FilteringFunctions/arm_biquad_cascade_stereo_df2T_f32.c
            DSP/Source/FilteringFunctions/arm_biquad_cascade_stereo_df2T_init_f32.c
            DSP/Source/FilteringFunctions/arm_conv_f32.c
            DSP/Source/FilteringFunctions/arm_conv_fast_opt_q15.c
            DSP/Source/FilteringFunctions/arm_conv_fast_q15.c
            DSP/Source/FilteringFunctions/arm_conv_fast_q31.c
            DSP/Source/FilteringFunctions/arm_conv_opt_q15.c
            DSP/Source/FilteringFunctions/arm_conv_opt_q7.c
            DSP/Source/FilteringFunctions/arm_conv_partial_f32.c
            DSP/Source/FilteringFunctions/arm_conv_partial_fast_opt_q15.c
            DSP/Source/FilteringFunctions/arm_conv_partial_fast_q15.c
            DSP/Source/FilteringFunctions/arm_conv_partial_fast_q31.c
            DSP/Source/FilteringFunctions/arm_conv_partial_opt_q15.c
            DSP/Source/FilteringFunctions/arm_conv_partial_opt_q7.c
            DSP/Source/FilteringFunctions/arm_conv_partial_q15.c
            DSP/Source/FilteringFunctions/arm_conv_partial_q31.c
            DSP/Source/FilteringFunctions/arm_conv_partial_q7.c
            DSP/Source/FilteringFunctions/arm_conv_q15.c
            DSP/Source/FilteringFunctions/arm_conv_q31.c
            DSP/Source/FilteringFunctions/arm_conv_q7.c
            DSP/Source/FilteringFunctions/arm_correlate_f32.c
            DSP/Source/FilteringFunctions/arm_correlate_f64.c
            DSP/Source/FilteringFunctions/arm_correlate_fast_opt_q15.c
            DSP/Source/FilteringFunctions/arm_correlate_fast_q15.c
            DSP/Source/FilteringFunctions/arm_correlate_fast_q31.c
            DSP/Source/FilteringFunctions/arm_correlate_opt_q15.c
            DSP/Source/FilteringFunctions/arm_correlate_opt_q7.c
            DSP/Source/FilteringFunctions/arm_correlate_q15.c
            DSP/Source/FilteringFunctions/arm_correlate_q31.c
            DSP/Source/FilteringFunctions/arm_correlate_q7.c
            DSP/Source/FilteringFunctions/arm_fir_decimate_f32.c
            DSP/Source/FilteringFunctions/arm_fir_decimate_f64.c
            DSP/Source/FilteringFunctions/arm_fir_decimate_fast_q15.c
            DSP/Source/FilteringFunctions/arm_fir_decimate_fast_q31.c
            DSP/Source/FilteringFunctions/arm_fir_decimate_init_f32.c
            DSP/Source/FilteringFunctions/arm_fir_decimate_init_f64.c
            DSP/Source/FilteringFunctions/arm_fir_decimate_init_q15.c
            DSP/Source/FilteringFunctions/arm_fir_decimate_init_q31.c
            DSP/Source/FilteringFunctions/arm_fir_decimate_q15.c
            DSP/Source/FilteringFunctions/arm_fir_decimate_q31.c
            DSP/Source/FilteringFunctions/arm_fir_f32.c
            DSP/Source/FilteringFunctions/arm_fir_f64.c
            DSP/Source/FilteringFunctions/arm_fir_fast_q15.c
            DSP/Source/FilteringFunctions/arm_fir_fast_q31.c
            DSP/Source/FilteringFunctions/arm_fir_init_f32.c
            DSP/Source/FilteringFunctions/arm_fir_init_f64.c
            DSP/Source/FilteringFunctions/arm_fir_init_q15.c
            DSP/Source/FilteringFunctions/arm_fir_init_q31.c
            DSP/Source/FilteringFunctions/arm_fir_init_q7.c
            DSP/Source/FilteringFunctions/arm_fir_interpolate_f32.c
            DSP/Source/FilteringFunctions/arm_fir_interpolate_init_f32.c
            DSP/Source/FilteringFunctions/arm_fir_interpolate_init_q15.c
            DSP/Source/FilteringFunctions/arm_fir_interpolate_init_q31.c
            DSP/Source/FilteringFunctions/arm_fir_interpolate_q15.c
            DSP/Source/FilteringFunctions/arm_fir_interpolate_q31.c
            DSP/Source/FilteringFunctions/arm_fir_lattice_f32.c
            DSP/Source/FilteringFunctions/arm_fir_lattice_init_f32.c
            DSP/Source/FilteringFunctions/arm_fir_lattice_init_q15.c
            DSP/Source/FilteringFunctions/arm_fir_lattice_init_q31.c
            DSP/Source/FilteringFunctions/arm_fir_lattice_q15.c
            DSP/Source/FilteringFunctions/arm_fir_lattice_q31.c
            DSP/Source/FilteringFunctions/arm_fir_q15.c
            DSP/Source/FilteringFunctions/arm_fir_q31.c
            DSP/Source/FilteringFunctions/arm_fir_q7.c
            DSP/Source/FilteringFunctions/arm_fir_sparse_f32.c
            DSP/Source/FilteringFunctions/arm_fir_sparse_init_f32.c
            DSP/Source/FilteringFunctions/arm_fir_sparse_init_q15.c
            DSP/Source/FilteringFunctions/arm_fir_sparse_init_q31.c
            DSP/Source/FilteringFunctions/arm_fir_sparse_init_q7.c
            DSP/Source/FilteringFunctions/arm_fir_sparse_q15.c
            DSP/Source/FilteringFunctions/arm_fir_sparse_q31.c
            DSP/Source/FilteringFunctions/arm_fir_sparse_q7.c
            DSP/Source/FilteringFunctions/arm_iir_lattice_f32.c
            DSP/Source/FilteringFunctions/arm_iir_lattice_init_f32.c
            DSP/Source/FilteringFunctions/arm_iir_lattice_init_q15.c
            DSP/Source/FilteringFunctions/arm_iir_lattice_init_q31.c
            DSP/Source/FilteringFunctions/arm_iir_lattice_q15.c
            DSP/Source/FilteringFunctions/arm_iir_lattice_q31.c
            DSP/Source/FilteringFunctions/arm_levinson_durbin_f32.c
            DSP/Source/FilteringFunctions/arm_levinson_durbin_q31.c
            DSP/Source/FilteringFunctions/arm_lms_f32.c
            DSP/Source/FilteringFunctions/arm_lms_init_f32.c
            DSP/Source/FilteringFunctions/arm_lms_init_q15.c
            DSP/Source/FilteringFunctions/arm_lms_init_q31.c
            DSP/Source/FilteringFunctions/arm_lms_norm_f32.c
            DSP/Source/FilteringFunctions/arm_lms_norm_init_f32.c
            DSP/Source/FilteringFunctions/arm_lms_norm_init_q15.c
            DSP/Source/FilteringFunctions/arm_lms_norm_init_q31.c
            DSP/Source/FilteringFunctions/arm_lms_norm_q15.c
            DSP/Source/FilteringFunctions/arm_lms_norm_q31.c
            DSP/Source/FilteringFunctions/arm_lms_q15.c
            DSP/Source/FilteringFunctions/arm_lms_q31.c
            DSP/Source/FilteringFunctions/arm_biquad_cascade_df1_f16.c
            DSP/Source/FilteringFunctions/arm_biquad_cascade_df1_init_f16.c
            DSP/Source/FilteringFunctions/arm_biquad_cascade_df2T_f16.c
            DSP/Source/FilteringFunctions/arm_biquad_cascade_df2T_init_f16.c
            DSP/Source/FilteringFunctions/arm_biquad_cascade_stereo_df2T_f16.c
            DSP/Source/FilteringFunctions/arm_biquad_cascade_stereo_df2T_init_f16.c
            DSP/Source/FilteringFunctions/arm_correlate_f16.c
            DSP/Source/FilteringFunctions/arm_fir_f16.c
            DSP/Source/FilteringFunctions/arm_fir_init_f16.c
            DSP/Source/FilteringFunctions/arm_levinson_durbin_f16.c
            DSP/Source/InterpolationFunctions/arm_bilinear_interp_f32.c
            DSP/Source/InterpolationFunctions/arm_bilinear_interp_q15.c
            DSP/Source/InterpolationFunctions/arm_bilinear_interp_q31.c
            DSP/Source/InterpolationFunctions/arm_bilinear_interp_q7.c
            DSP/Source/InterpolationFunctions/arm_linear_interp_f32.c
            DSP/Source/InterpolationFunctions/arm_linear_interp_q15.c
            DSP/Source/InterpolationFunctions/arm_linear_interp_q31.c
            DSP/Source/InterpolationFunctions/arm_linear_interp_q7.c
            DSP/Source/InterpolationFunctions/arm_spline_interp_f32.c
            DSP/Source/InterpolationFunctions/arm_spline_interp_init_f32.c
            DSP/Source/InterpolationFunctions/arm_bilinear_interp_f16.c
            DSP/Source/InterpolationFunctions/arm_linear_interp_f16.c
            DSP/Source/MatrixFunctions/arm_householder_f32.c
            DSP/Source/MatrixFunctions/arm_householder_f64.c
            DSP/Source/MatrixFunctions/arm_mat_add_f32.c
            DSP/Source/MatrixFunctions/arm_mat_add_q15.c
            DSP/Source/MatrixFunctions/arm_mat_add_q31.c
            DSP/Source/MatrixFunctions/arm_mat_cholesky_f32.c
            DSP/Source/MatrixFunctions/arm_mat_cholesky_f64.c
            DSP/Source/MatrixFunctions/arm_mat_cmplx_mult_f32.c
            DSP/Source/MatrixFunctions/arm_mat_cmplx_mult_q15.c
            DSP/Source/MatrixFunctions/arm_mat_cmplx_mult_q31.c
            DSP/Source/MatrixFunctions/arm_mat_cmplx_trans_f32.c
            DSP/Source/MatrixFunctions/arm_mat_cmplx_trans_q15.c
            DSP/Source/MatrixFunctions/arm_mat_cmplx_trans_q31.c
            DSP/Source/MatrixFunctions/arm_mat_init_f32.c
            DSP/Source/MatrixFunctions/arm_mat_init_f64.c
            DSP/Source/MatrixFunctions/arm_mat_init_q15.c
            DSP/Source/MatrixFunctions/arm_mat_init_q31.c
            DSP/Source/MatrixFunctions/arm_mat_inverse_f32.c
            DSP/Source/MatrixFunctions/arm_mat_inverse_f64.c
            DSP/Source/MatrixFunctions/arm_mat_ldlt_f32.c
            DSP/Source/MatrixFunctions/arm_mat_ldlt_f64.c
            DSP/Source/MatrixFunctions/arm_mat_mult_f32.c
            DSP/Source/MatrixFunctions/arm_mat_mult_f64.c
            DSP/Source/MatrixFunctions/arm_mat_mult_fast_q15.c
            DSP/Source/MatrixFunctions/arm_mat_mult_fast_q31.c
            DSP/Source/MatrixFunctions/arm_mat_mult_opt_q31.c
            DSP/Source/MatrixFunctions/arm_mat_mult_q15.c
            DSP/Source/MatrixFunctions/arm_mat_mult_q31.c
            DSP/Source/MatrixFunctions/arm_mat_mult_q7.c
            DSP/Source/MatrixFunctions/arm_mat_qr_f32.c
            DSP/Source/MatrixFunctions/arm_mat_qr_f64.c
            DSP/Source/MatrixFunctions/arm_mat_scale_f32.c
            DSP/Source/MatrixFunctions/arm_mat_scale_q15.c
            DSP/Source/MatrixFunctions/arm_mat_scale_q31.c
            DSP/Source/MatrixFunctions/arm_mat_solve_lower_triangular_f32.c
            DSP/Source/MatrixFunctions/arm_mat_solve_lower_triangular_f64.c
            DSP/Source/MatrixFunctions/arm_mat_solve_upper_triangular_f32.c
            DSP/Source/MatrixFunctions/arm_mat_solve_upper_triangular_f64.c
            DSP/Source/MatrixFunctions/arm_mat_sub_f32.c
            DSP/Source/MatrixFunctions/arm_mat_sub_f64.c
            DSP/Source/MatrixFunctions/arm_mat_sub_q15.c
            DSP/Source/MatrixFunctions/arm_mat_sub_q31.c
            DSP/Source/MatrixFunctions/arm_mat_trans_f32.c
            DSP/Source/MatrixFunctions/arm_mat_trans_f64.c
            DSP/Source/MatrixFunctions/arm_mat_trans_q15.c
            DSP/Source/MatrixFunctions/arm_mat_trans_q31.c
            DSP/Source/MatrixFunctions/arm_mat_trans_q7.c
            DSP/Source/MatrixFunctions/arm_mat_vec_mult_f32.c
            DSP/Source/MatrixFunctions/arm_mat_vec_mult_q15.c
            DSP/Source/MatrixFunctions/arm_mat_vec_mult_q31.c
            DSP/Source/MatrixFunctions/arm_mat_vec_mult_q7.c
            DSP/Source/MatrixFunctions/arm_householder_f16.c
            DSP/Source/MatrixFunctions/arm_mat_add_f16.c
            DSP/Source/MatrixFunctions/arm_mat_cholesky_f16.c
            DSP/Source/MatrixFunctions/arm_mat_cmplx_mult_f16.c
            DSP/Source/MatrixFunctions/arm_mat_cmplx_trans_f16.c
            DSP/Source/MatrixFunctions/arm_mat_init_f16.c
            DSP/Source/MatrixFunctions/arm_mat_inverse_f16.c
            DSP/Source/MatrixFunctions/arm_mat_qr_f16.c
            DSP/Source/MatrixFunctions/arm_mat_mult_f16.c
            DSP/Source/MatrixFunctions/arm_mat_scale_f16.c
            DSP/Source/MatrixFunctions/arm_mat_solve_lower_triangular_f16.c
            DSP/Source/MatrixFunctions/arm_mat_solve_upper_triangular_f16.c
            DSP/Source/MatrixFunctions/arm_mat_sub_f16.c
            DSP/Source/MatrixFunctions/arm_mat_trans_f16.c
            DSP/Source/MatrixFunctions/arm_mat_vec_mult_f16.c
            DSP/Source/QuaternionMathFunctions/arm_quaternion2rotation_f32.c
            DSP/Source/QuaternionMathFunctions/arm_quaternion_conjugate_f32.c
            DSP/Source/QuaternionMathFunctions/arm_quaternion_inverse_f32.c
            DSP/Source/QuaternionMathFunctions/arm_quaternion_normalize_f32.c
            DSP/Source/QuaternionMathFunctions/arm_quaternion_norm_f32.c
            DSP/Source/QuaternionMathFunctions/arm_quaternion_product_f32.c
            DSP/Source/QuaternionMathFunctions/arm_quaternion_product_single_f32.c
            DSP/Source/QuaternionMathFunctions/arm_rotation2quaternion_f32.c
            DSP/Source/SVMFunctions/arm_svm_linear_init_f32.c
            DSP/Source/SVMFunctions/arm_svm_linear_predict_f32.c
            DSP/Source/SVMFunctions/arm_svm_polynomial_init_f32.c
            DSP/Source/SVMFunctions/arm_svm_polynomial_predict_f32.c
            DSP/Source/SVMFunctions/arm_svm_rbf_init_f32.c
            DSP/Source/SVMFunctions/arm_svm_rbf_predict_f32.c
            DSP/Source/SVMFunctions/arm_svm_sigmoid_init_f32.c
            DSP/Source/SVMFunctions/arm_svm_sigmoid_predict_f32.c
            DSP/Source/SVMFunctions/arm_svm_linear_init_f16.c
            DSP/Source/SVMFunctions/arm_svm_linear_predict_f16.c
            DSP/Source/SVMFunctions/arm_svm_polynomial_init_f16.c
            DSP/Source/SVMFunctions/arm_svm_polynomial_predict_f16.c
            DSP/Source/SVMFunctions/arm_svm_rbf_init_f16.c
            DSP/Source/SVMFunctions/arm_svm_rbf_predict_f16.c
            DSP/Source/SVMFunctions/arm_svm_sigmoid_init_f16.c
            DSP/Source/SVMFunctions/arm_svm_sigmoid_predict_f16.c
            DSP/Source/StatisticsFunctions/arm_absmax_f32.c
            DSP/Source/StatisticsFunctions/arm_absmax_f64.c
            DSP/Source/StatisticsFunctions/arm_absmax_no_idx_f32.c
            DSP/Source/StatisticsFunctions/arm_absmax_no_idx_f64.c
            DSP/Source/StatisticsFunctions/arm_absmax_no_idx_q15.c
            DSP/Source/StatisticsFunctions/arm_absmax_no_idx_q31.c
            DSP/Source/StatisticsFunctions/arm_absmax_no_idx_q7.c
            DSP/Source/StatisticsFunctions/arm_absmax_q15.c
            DSP/Source/StatisticsFunctions/arm_absmax_q31.c
            DSP/Source/StatisticsFunctions/arm_absmax_q7.c
            DSP/Source/StatisticsFunctions/arm_absmin_f32.c
            DSP/Source/StatisticsFunctions/arm_absmin_f64.c
            DSP/Source/StatisticsFunctions/arm_absmin_no_idx_f32.c
            DSP/Source/StatisticsFunctions/arm_absmin_no_idx_f64.c
            DSP/Source/StatisticsFunctions/arm_absmin_no_idx_q15.c
            DSP/Source/StatisticsFunctions/arm_absmin_no_idx_q31.c
            DSP/Source/StatisticsFunctions/arm_absmin_no_idx_q7.c
            DSP/Source/StatisticsFunctions/arm_absmin_q15.c
            DSP/Source/StatisticsFunctions/arm_absmin_q31.c
            DSP/Source/StatisticsFunctions/arm_absmin_q7.c
            DSP/Source/StatisticsFunctions/arm_accumulate_f32.c
            DSP/Source/StatisticsFunctions/arm_accumulate_f64.c
            DSP/Source/StatisticsFunctions/arm_entropy_f32.c
            DSP/Source/StatisticsFunctions/arm_entropy_f64.c
            DSP/Source/StatisticsFunctions/arm_kullback_leibler_f32.c
            DSP/Source/StatisticsFunctions/arm_kullback_leibler_f64.c
            DSP/Source/StatisticsFunctions/arm_logsumexp_dot_prod_f32.c
            DSP/Source/StatisticsFunctions/arm_logsumexp_f32.c
            DSP/Source/StatisticsFunctions/arm_max_f32.c
            DSP/Source/StatisticsFunctions/arm_max_f64.c
            DSP/Source/StatisticsFunctions/arm_max_no_idx_f32.c
            DSP/Source/StatisticsFunctions/arm_max_no_idx_f64.c
            DSP/Source/StatisticsFunctions/arm_max_no_idx_q15.c
            DSP/Source/StatisticsFunctions/arm_max_no_idx_q31.c
            DSP/Source/StatisticsFunctions/arm_max_no_idx_q7.c
            DSP/Source/StatisticsFunctions/arm_max_q15.c
            DSP/Source/StatisticsFunctions/arm_max_q31.c
            DSP/Source/StatisticsFunctions/arm_max_q7.c
            DSP/Source/StatisticsFunctions/arm_mean_f32.c
            DSP/Source/StatisticsFunctions/arm_mean_f64.c
            DSP/Source/StatisticsFunctions/arm_mean_q15.c
            DSP/Source/StatisticsFunctions/arm_mean_q31.c
            DSP/Source/StatisticsFunctions/arm_mean_q7.c
            DSP/Source/StatisticsFunctions/arm_min_f32.c
            DSP/Source/StatisticsFunctions/arm_min_f64.c
            DSP/Source/StatisticsFunctions/arm_min_no_idx_f32.c
            DSP/Source/StatisticsFunctions/arm_min_no_idx_f64.c
            DSP/Source/StatisticsFunctions/arm_min_no_idx_q15.c
            DSP/Source/StatisticsFunctions/arm_min_no_idx_q31.c
            DSP/Source/StatisticsFunctions/arm_min_no_idx_q7.c
            DSP/Source/StatisticsFunctions/arm_min_q15.c
            DSP/Source/StatisticsFunctions/arm_min_q31.c
            DSP/Source/StatisticsFunctions/arm_min_q7.c
            DSP/Source/StatisticsFunctions/arm_mse_f32.c
            DSP/Source/StatisticsFunctions/arm_mse_f64.c
            DSP/Source/StatisticsFunctions/arm_mse_q15.c
            DSP/Source/StatisticsFunctions/arm_mse_q31.c
            DSP/Source/StatisticsFunctions/arm_mse_q7.c
            DSP/Source/StatisticsFunctions/arm_power_f32.c
            DSP/Source/StatisticsFunctions/arm_power_f64.c
            DSP/Source/StatisticsFunctions/arm_power_q15.c
            DSP/Source/StatisticsFunctions/arm_power_q31.c
            DSP/Source/StatisticsFunctions/arm_power_q7.c
            DSP/Source/StatisticsFunctions/arm_rms_f32.c
            DSP/Source/StatisticsFunctions/arm_rms_q15.c
            DSP/Source/StatisticsFunctions/arm_rms_q31.c
            DSP/Source/StatisticsFunctions/arm_std_f32.c
            DSP/Source/StatisticsFunctions/arm_std_f64.c
            DSP/Source/StatisticsFunctions/arm_std_q15.c
            DSP/Source/StatisticsFunctions/arm_std_q31.c
            DSP/Source/StatisticsFunctions/arm_var_f32.c
            DSP/Source/StatisticsFunctions/arm_var_f64.c
            DSP/Source/StatisticsFunctions/arm_var_q15.c
            DSP/Source/StatisticsFunctions/arm_var_q31.c
            DSP/Source/StatisticsFunctions/arm_absmax_f16.c
            DSP/Source/StatisticsFunctions/arm_absmax_no_idx_f16.c
            DSP/Source/StatisticsFunctions/arm_absmin_f16.c
            DSP/Source/StatisticsFunctions/arm_absmin_no_idx_f16.c
            DSP/Source/StatisticsFunctions/arm_accumulate_f16.c
            DSP/Source/StatisticsFunctions/arm_entropy_f16.c
            DSP/Source/StatisticsFunctions/arm_kullback_leibler_f16.c
            DSP/Source/StatisticsFunctions/arm_logsumexp_dot_prod_f16.c
            DSP/Source/StatisticsFunctions/arm_logsumexp_f16.c
            DSP/Source/StatisticsFunctions/arm_max_f16.c
            DSP/Source/StatisticsFunctions/arm_max_no_idx_f16.c
            DSP/Source/StatisticsFunctions/arm_mean_f16.c
            DSP/Source/StatisticsFunctions/arm_min_f16.c
            DSP/Source/StatisticsFunctions/arm_min_no_idx_f16.c
            DSP/Source/StatisticsFunctions/arm_mse_f16.c
            DSP/Source/StatisticsFunctions/arm_power_f16.c
            DSP/Source/StatisticsFunctions/arm_rms_f16.c
            DSP/Source/StatisticsFunctions/arm_std_f16.c
            DSP/Source/StatisticsFunctions/arm_var_f16.c
            DSP/Source/SupportFunctions/arm_barycenter_f32.c
            DSP/Source/SupportFunctions/arm_bitonic_sort_f32.c
            DSP/Source/SupportFunctions/arm_bubble_sort_f32.c
            DSP/Source/SupportFunctions/arm_copy_f32.c
            DSP/Source/SupportFunctions/arm_copy_f64.c
            DSP/Source/SupportFunctions/arm_copy_q15.c
            DSP/Source/SupportFunctions/arm_copy_q31.c
            DSP/Source/SupportFunctions/arm_copy_q7.c
            DSP/Source/SupportFunctions/arm_f64_to_float.c
            DSP/Source/SupportFunctions/arm_f64_to_q31.c
            DSP/Source/SupportFunctions/arm_f64_to_q15.c
            DSP/Source/SupportFunctions/arm_f64_to_q7.c
            DSP/Source/SupportFunctions/arm_fill_f32.c
            DSP/Source/SupportFunctions/arm_fill_f64.c
            DSP/Source/SupportFunctions/arm_fill_q15.c
            DSP/Source/SupportFunctions/arm_fill_q31.c
            DSP/Source/SupportFunctions/arm_fill_q7.c
            DSP/Source/SupportFunctions/arm_float_to_f64.c
            DSP/Source/SupportFunctions/arm_float_to_q15.c
            DSP/Source/SupportFunctions/arm_float_to_q31.c
            DSP/Source/SupportFunctions/arm_float_to_q7.c
            DSP/Source/SupportFunctions/arm_heap_sort_f32.c
            DSP/Source/SupportFunctions/arm_insertion_sort_f32.c
            DSP/Source/SupportFunctions/arm_merge_sort_f32.c
            DSP/Source/SupportFunctions/arm_merge_sort_init_f32.c
            DSP/Source/SupportFunctions/arm_q15_to_f64.c
            DSP/Source/SupportFunctions/arm_q15_to_float.c
            DSP/Source/SupportFunctions/arm_q15_to_q31.c
            DSP/Source/SupportFunctions/arm_q15_to_q7.c
            DSP/Source/SupportFunctions/arm_q31_to_f64.c
            DSP/Source/SupportFunctions/arm_q31_to_float.c
            DSP/Source/SupportFunctions/arm_q31_to_q15.c
            DSP/Source/SupportFunctions/arm_q31_to_q7.c
            DSP/Source/SupportFunctions/arm_q7_to_f64.c
            DSP/Source/SupportFunctions/arm_q7_to_float.c
            DSP/Source/SupportFunctions/arm_q7_to_q15.c
            DSP/Source/SupportFunctions/arm_q7_to_q31.c
            DSP/Source/SupportFunctions/arm_quick_sort_f32.c
            DSP/Source/SupportFunctions/arm_selection_sort_f32.c
            DSP/Source/SupportFunctions/arm_sort_f32.c
            DSP/Source/SupportFunctions/arm_sort_init_f32.c
            DSP/Source/SupportFunctions/arm_weighted_average_f32.c
            DSP/Source/SupportFunctions/arm_barycenter_f16.c
            DSP/Source/SupportFunctions/arm_copy_f16.c
            DSP/Source/SupportFunctions/arm_f16_to_float.c
            DSP/Source/SupportFunctions/arm_f16_to_q15.c
            DSP/Source/SupportFunctions/arm_f16_to_f64.c
            DSP/Source/SupportFunctions/arm_f64_to_f16.c
            DSP/Source/SupportFunctions/arm_fill_f16.c
            DSP/Source/SupportFunctions/arm_float_to_f16.c
            DSP/Source/SupportFunctions/arm_q15_to_f16.c
            DSP/Source/SupportFunctions/arm_weighted_average_f16.c
            DSP/Source/TransformFunctions/arm_bitreversal.c
            DSP/Source/TransformFunctions/arm_bitreversal2.c
            DSP/Source/TransformFunctions/arm_cfft_f32.c
            DSP/Source/TransformFunctions/arm_cfft_f64.c
            DSP/Source/TransformFunctions/arm_cfft_init_f32.c
            DSP/Source/TransformFunctions/arm_cfft_init_f64.c
            DSP/Source/TransformFunctions/arm_cfft_init_q15.c
            DSP/Source/TransformFunctions/arm_cfft_init_q31.c
            DSP/Source/TransformFunctions/arm_cfft_q15.c
            DSP/Source/TransformFunctions/arm_cfft_q31.c
            DSP/Source/TransformFunctions/arm_cfft_radix2_f32.c
            DSP/Source/TransformFunctions/arm_cfft_radix2_init_f32.c
            DSP/Source/TransformFunctions/arm_cfft_radix2_init_q15.c
            DSP/Source/TransformFunctions/arm_cfft_radix2_init_q31.c
            DSP/Source/TransformFunctions/arm_cfft_radix2_q15.c
            DSP/Source/TransformFunctions/arm_cfft_radix2_q31.c
            DSP/Source/TransformFunctions/arm_cfft_radix4_f32.c
            DSP/Source/TransformFunctions/arm_cfft_radix4_init_f32.c
            DSP/Source/TransformFunctions/arm_cfft_radix4_init_q15.c
            DSP/Source/TransformFunctions/arm_cfft_radix4_init_q31.c
            DSP/Source/TransformFunctions/arm_cfft_radix4_q15.c
            DSP/Source/TransformFunctions/arm_cfft_radix4_q31.c
            DSP/Source/TransformFunctions/arm_cfft_radix8_f32.c
            DSP/Source/TransformFunctions/arm_dct4_f32.c
            DSP/Source/TransformFunctions/arm_dct4_init_f32.c
            DSP/Source/TransformFunctions/arm_dct4_init_q15.c
            DSP/Source/TransformFunctions/arm_dct4_init_q31.c
            DSP/Source/TransformFunctions/arm_dct4_q15.c
            DSP/Source/TransformFunctions/arm_dct4_q31.c
            DSP/Source/TransformFunctions/arm_mfcc_f32.c
            DSP/Source/TransformFunctions/arm_mfcc_init_f32.c
            DSP/Source/TransformFunctions/arm_mfcc_init_q15.c
            DSP/Source/TransformFunctions/arm_mfcc_init_q31.c
            DSP/Source/TransformFunctions/arm_mfcc_q15.c
            DSP/Source/TransformFunctions/arm_mfcc_q31.c
            DSP/Source/TransformFunctions/arm_rfft_f32.c
            DSP/Source/TransformFunctions/arm_rfft_fast_f32.c
            DSP/Source/TransformFunctions/arm_rfft_fast_f64.c
            DSP/Source/TransformFunctions/arm_rfft_fast_init_f32.c
            DSP/Source/TransformFunctions/arm_rfft_fast_init_f64.c
            DSP/Source/TransformFunctions/arm_rfft_init_f32.c
            DSP/Source/TransformFunctions/arm_rfft_init_q15.c
            DSP/Source/TransformFunctions/arm_rfft_init_q31.c
            DSP/Source/TransformFunctions/arm_rfft_q15.c
            DSP/Source/TransformFunctions/arm_rfft_q31.c
            DSP/Source/TransformFunctions/arm_bitreversal_f16.c
            DSP/Source/TransformFunctions/arm_cfft_f16.c
            DSP/Source/TransformFunctions/arm_cfft_init_f16.c
            DSP/Source/TransformFunctions/arm_cfft_radix2_f16.c
            DSP/Source/TransformFunctions/arm_cfft_radix2_init_f16.c
            DSP/Source/TransformFunctions/arm_cfft_radix4_f16.c
            DSP/Source/TransformFunctions/arm_cfft_radix8_f16.c
            DSP/Source/TransformFunctions/arm_mfcc_f16.c
            DSP/Source/TransformFunctions/arm_cfft_radix4_init_f16.c
            DSP/Source/TransformFunctions/arm_mfcc_init_f16.c
            DSP/Source/TransformFunctions/arm_rfft_fast_f16.c
            DSP/Source/TransformFunctions/arm_rfft_fast_init_f16.c
            DSP/Source/WindowFunctions/arm_bartlett_f32.c
            DSP/Source/WindowFunctions/arm_bartlett_f64.c
            DSP/Source/WindowFunctions/arm_blackman_harris_92db_f32.c
            DSP/Source/WindowFunctions/arm_blackman_harris_92db_f64.c
            DSP/Source/WindowFunctions/arm_hamming_f32.c
            DSP/Source/WindowFunctions/arm_hamming_f64.c
            DSP/Source/WindowFunctions/arm_hanning_f32.c
            DSP/Source/WindowFunctions/arm_hanning_f64.c
            DSP/Source/WindowFunctions/arm_hft116d_f32.c
            DSP/Source/WindowFunctions/arm_hft116d_f64.c
            DSP/Source/WindowFunctions/arm_hft144d_f32.c
            DSP/Source/WindowFunctions/arm_hft144d_f64.c
            DSP/Source/WindowFunctions/arm_hft169d_f32.c
            DSP/Source/WindowFunctions/arm_hft169d_f64.c
            DSP/Source/WindowFunctions/arm_hft196d_f32.c
            DSP/Source/WindowFunctions/arm_hft196d_f64.c
            DSP/Source/WindowFunctions/arm_hft223d_f32.c
            DSP/Source/WindowFunctions/arm_hft223d_f64.c
            DSP/Source/WindowFunctions/arm_hft248d_f32.c
            DSP/Source/WindowFunctions/arm_hft248d_f64.c
            DSP/Source/WindowFunctions/arm_hft90d_f32.c
            DSP/Source/WindowFunctions/arm_hft90d_f64.c
            DSP/Source/WindowFunctions/arm_hft95_f32.c
            DSP/Source/WindowFunctions/arm_hft95_f64.c
            DSP/Source/WindowFunctions/arm_nuttall3a_f32.c
            DSP/Source/WindowFunctions/arm_nuttall3a_f64.c
            DSP/Source/WindowFunctions/arm_nuttall3b_f32.c
            DSP/Source/WindowFunctions/arm_nuttall3b_f64.c
            DSP/Source/WindowFunctions/arm_nuttall3_f32.c
            DSP/Source/WindowFunctions/arm_nuttall3_f64.c
            DSP/Source/WindowFunctions/arm_nuttall4a_f32.c
            DSP/Source/WindowFunctions/arm_nuttall4a_f64.c
            DSP/Source/WindowFunctions/arm_nuttall4b_f32.c
            DSP/Source/WindowFunctions/arm_nuttall4b_f64.c
            DSP/Source/WindowFunctions/arm_nuttall4c_f32.c
            DSP/Source/WindowFunctions/arm_nuttall4c_f64.c
            DSP/Source/WindowFunctions/arm_nuttall4_f32.c
            DSP/Source/WindowFunctions/arm_nuttall4_f64.c
            DSP/Source/WindowFunctions/arm_welch_f32.c
            DSP/Source/WindowFunctions/arm_welch_f64.c
    )

    mcux_add_include(
        INCLUDES
            DSP/Include
            DSP/PrivateInclude
            DSP/Source/DistanceFunctions
    )

endif()

if (CONFIG_MCUX_COMPONENT_CMSIS_NN_Source)
    mcux_add_source(
        SOURCES
            NN/Include/arm_nnfunctions.h
            NN/Include/arm_nnsupportfunctions.h
            NN/Include/arm_nn_math_types.h
            NN/Include/arm_nn_tables.h
            NN/Include/arm_nn_types.h
            NN/Include/Internal/arm_nn_compiler.h
            NN/Source/ActivationFunctions/arm_nn_activation_s16.c
            NN/Source/ActivationFunctions/arm_relu6_s8.c
            NN/Source/ActivationFunctions/arm_relu_q15.c
            NN/Source/ActivationFunctions/arm_relu_q7.c
            NN/Source/BasicMathFunctions/arm_elementwise_add_s16.c
            NN/Source/BasicMathFunctions/arm_elementwise_add_s8.c
            NN/Source/BasicMathFunctions/arm_elementwise_mul_acc_s16.c
            NN/Source/BasicMathFunctions/arm_elementwise_mul_s16.c
            NN/Source/BasicMathFunctions/arm_elementwise_mul_s16_s8.c
            NN/Source/BasicMathFunctions/arm_elementwise_mul_s8.c
            NN/Source/BasicMathFunctions/arm_elementwise_mul_s16_batch_offset.c
            NN/Source/ConcatenationFunctions/arm_concatenation_s8_w.c
            NN/Source/ConcatenationFunctions/arm_concatenation_s8_x.c
            NN/Source/ConcatenationFunctions/arm_concatenation_s8_y.c
            NN/Source/ConcatenationFunctions/arm_concatenation_s8_z.c
            NN/Source/ConvolutionFunctions/arm_convolve_1x1_s4.c
            NN/Source/ConvolutionFunctions/arm_convolve_1x1_s4_fast.c
            NN/Source/ConvolutionFunctions/arm_convolve_1x1_s8.c
            NN/Source/ConvolutionFunctions/arm_convolve_1x1_s8_fast.c
            NN/Source/ConvolutionFunctions/arm_convolve_1_x_n_s4.c
            NN/Source/ConvolutionFunctions/arm_convolve_1_x_n_s8.c
            NN/Source/ConvolutionFunctions/arm_convolve_get_buffer_sizes_s16.c
            NN/Source/ConvolutionFunctions/arm_convolve_get_buffer_sizes_s4.c
            NN/Source/ConvolutionFunctions/arm_convolve_get_buffer_sizes_s8.c
            NN/Source/ConvolutionFunctions/arm_convolve_s16.c
            NN/Source/ConvolutionFunctions/arm_convolve_s4.c
            NN/Source/ConvolutionFunctions/arm_convolve_s8.c
            NN/Source/ConvolutionFunctions/arm_convolve_wrapper_s16.c
            NN/Source/ConvolutionFunctions/arm_convolve_wrapper_s4.c
            NN/Source/ConvolutionFunctions/arm_convolve_wrapper_s8.c
            NN/Source/ConvolutionFunctions/arm_depthwise_conv_3x3_s8.c
            NN/Source/ConvolutionFunctions/arm_depthwise_conv_fast_s16.c
            NN/Source/ConvolutionFunctions/arm_depthwise_conv_get_buffer_sizes_s16.c
            NN/Source/ConvolutionFunctions/arm_depthwise_conv_get_buffer_sizes_s4.c
            NN/Source/ConvolutionFunctions/arm_depthwise_conv_get_buffer_sizes_s8.c
            NN/Source/ConvolutionFunctions/arm_depthwise_conv_s16.c
            NN/Source/ConvolutionFunctions/arm_depthwise_conv_s4.c
            NN/Source/ConvolutionFunctions/arm_depthwise_conv_s4_opt.c
            NN/Source/ConvolutionFunctions/arm_depthwise_conv_s8.c
            NN/Source/ConvolutionFunctions/arm_depthwise_conv_s8_opt.c
            NN/Source/ConvolutionFunctions/arm_depthwise_conv_wrapper_s16.c
            NN/Source/ConvolutionFunctions/arm_depthwise_conv_wrapper_s4.c
            NN/Source/ConvolutionFunctions/arm_depthwise_conv_wrapper_s8.c
            NN/Source/ConvolutionFunctions/arm_nn_depthwise_conv_s8_core.c
            NN/Source/ConvolutionFunctions/arm_nn_mat_mult_kernel_row_offset_s8_s16.c
            NN/Source/ConvolutionFunctions/arm_nn_mat_mult_kernel_s4_s16.c
            NN/Source/ConvolutionFunctions/arm_nn_mat_mult_kernel_s8_s16.c
            NN/Source/ConvolutionFunctions/arm_nn_mat_mult_kernel_s16.c
            NN/Source/ConvolutionFunctions/arm_nn_mat_mult_s8.c
            NN/Source/ConvolutionFunctions/arm_transpose_conv_get_buffer_sizes_s8.c
            NN/Source/ConvolutionFunctions/arm_transpose_conv_s8.c
            NN/Source/FullyConnectedFunctions/arm_fully_connected_get_buffer_sizes_s16.c
            NN/Source/FullyConnectedFunctions/arm_fully_connected_get_buffer_sizes_s8.c
            NN/Source/FullyConnectedFunctions/arm_fully_connected_s16.c
            NN/Source/FullyConnectedFunctions/arm_fully_connected_s4.c
            NN/Source/FullyConnectedFunctions/arm_fully_connected_s8.c
            NN/Source/FullyConnectedFunctions/arm_vector_sum_s8.c
            NN/Source/FullyConnectedFunctions/arm_vector_sum_s8_s64.c
            NN/Source/LSTMFunctions/arm_lstm_unidirectional_s16.c
            NN/Source/LSTMFunctions/arm_lstm_unidirectional_s8.c
            NN/Source/NNSupportFunctions/arm_nntables.c
            NN/Source/NNSupportFunctions/arm_nn_depthwise_conv_nt_t_padded_s8.c
            NN/Source/NNSupportFunctions/arm_nn_depthwise_conv_nt_t_s16.c
            NN/Source/NNSupportFunctions/arm_nn_depthwise_conv_nt_t_s4.c
            NN/Source/NNSupportFunctions/arm_nn_depthwise_conv_nt_t_s8.c
            NN/Source/NNSupportFunctions/arm_nn_lstm_calculate_gate_s16.c
            NN/Source/NNSupportFunctions/arm_nn_lstm_calculate_gate_s8_s16.c
            NN/Source/NNSupportFunctions/arm_nn_lstm_step_s16.c
            NN/Source/NNSupportFunctions/arm_nn_lstm_step_s8.c
            NN/Source/NNSupportFunctions/arm_nn_mat_mult_nt_t_s16.c
            NN/Source/NNSupportFunctions/arm_nn_mat_mult_nt_t_s4.c
            NN/Source/NNSupportFunctions/arm_nn_mat_mult_nt_t_s8.c
            NN/Source/NNSupportFunctions/arm_nn_mat_mult_nt_t_s8_s32.c
            NN/Source/NNSupportFunctions/arm_nn_mat_mul_core_1x_s4.c
            NN/Source/NNSupportFunctions/arm_nn_mat_mul_core_1x_s8.c
            NN/Source/NNSupportFunctions/arm_nn_mat_mul_core_4x_s8.c
            NN/Source/NNSupportFunctions/arm_nn_vec_mat_mul_result_acc_s16.c
            NN/Source/NNSupportFunctions/arm_nn_vec_mat_mul_result_acc_s8_s16.c
            NN/Source/NNSupportFunctions/arm_nn_vec_mat_mult_t_s16.c
            NN/Source/NNSupportFunctions/arm_nn_vec_mat_mult_t_s4.c
            NN/Source/NNSupportFunctions/arm_nn_vec_mat_mult_t_s8.c
            NN/Source/NNSupportFunctions/arm_nn_vec_mat_mult_t_svdf_s8.c
            NN/Source/NNSupportFunctions/arm_q7_to_q15_with_offset.c
            NN/Source/NNSupportFunctions/arm_s8_to_s16_unordered_with_offset.c
            NN/Source/PoolingFunctions/arm_avgpool_get_buffer_sizes_s16.c
            NN/Source/PoolingFunctions/arm_avgpool_get_buffer_sizes_s8.c
            NN/Source/PoolingFunctions/arm_avgpool_s16.c
            NN/Source/PoolingFunctions/arm_avgpool_s8.c
            NN/Source/PoolingFunctions/arm_max_pool_s16.c
            NN/Source/PoolingFunctions/arm_max_pool_s8.c
            NN/Source/ReshapeFunctions/arm_reshape_s8.c
            NN/Source/SoftmaxFunctions/arm_nn_softmax_common_s8.c
            NN/Source/SoftmaxFunctions/arm_softmax_s16.c
            NN/Source/SoftmaxFunctions/arm_softmax_s8.c
            NN/Source/SoftmaxFunctions/arm_softmax_s8_s16.c
            NN/Source/SoftmaxFunctions/arm_softmax_u8.c
            NN/Source/SVDFunctions/arm_svdf_get_buffer_sizes_s8.c
            NN/Source/SVDFunctions/arm_svdf_s8.c
            NN/Source/SVDFunctions/arm_svdf_state_s16_s8.c
    )

    mcux_add_include(
        INCLUDES
            NN/Include
    )

endif()

if (CONFIG_MCUX_COMPONENT_CMSIS_Driver_Include.USART)
    mcux_add_source(
        SOURCES
            Driver/Include/Driver_USART.h
            Driver/Include/Driver_Common.h
    )

    mcux_add_include(
        INCLUDES
            Driver/Include
    )

endif()

if (CONFIG_MCUX_COMPONENT_CMSIS_Driver_Include.CAN)
    mcux_add_source(
        SOURCES
            Driver/Include/Driver_CAN.h
            Driver/Include/Driver_Common.h
    )

    mcux_add_include(
        INCLUDES
            Driver/Include
    )

endif()

if (CONFIG_MCUX_COMPONENT_CMSIS_Driver_Include.Ethernet)
    mcux_add_source(
        SOURCES
            Driver/Include/Driver_Common.h
            Driver/Include/Driver_ETH.h
            Driver/Include/Driver_ETH_MAC.h
            Driver/Include/Driver_ETH_PHY.h
    )

    mcux_add_include(
        INCLUDES
            Driver/Include
    )

endif()

if (CONFIG_MCUX_COMPONENT_CMSIS_Driver_Include.Ethernet_MAC)
    mcux_add_source(
        SOURCES
            Driver/Include/Driver_ETH.h
            Driver/Include/Driver_Common.h
            Driver/Include/Driver_ETH_MAC.h
    )

    mcux_add_include(
        INCLUDES
            Driver/Include
    )

endif()

if (CONFIG_MCUX_COMPONENT_CMSIS_Driver_Include.Ethernet_PHY)
    mcux_add_source(
        SOURCES
            Driver/Include/Driver_ETH.h
            Driver/Include/Driver_ETH_PHY.h
            Driver/Include/Driver_Common.h
    )

    mcux_add_include(
        INCLUDES
            Driver/Include
    )

endif()

if (CONFIG_MCUX_COMPONENT_CMSIS_Driver_Include.Flash)
    mcux_add_source(
        SOURCES
            Driver/Include/Driver_Flash.h
            Driver/Include/Driver_Common.h
    )

    mcux_add_include(
        INCLUDES
            Driver/Include
    )

endif()

if (CONFIG_MCUX_COMPONENT_CMSIS_Driver_Include.GPIO)
    mcux_add_source(
        SOURCES
            Driver/Include/Driver_GPIO.h
            Driver/Include/Driver_Common.h
    )

    mcux_add_include(
        INCLUDES
            Driver/Include
    )

endif()

if (CONFIG_MCUX_COMPONENT_CMSIS_Driver_Include.I2C)
    mcux_add_source(
        SOURCES
            Driver/Include/Driver_I2C.h
            Driver/Include/Driver_Common.h
    )

    mcux_add_include(
        INCLUDES
            Driver/Include
    )

endif()

if (CONFIG_MCUX_COMPONENT_CMSIS_Driver_Include.MCI)
    mcux_add_source(
        SOURCES
            Driver/Include/Driver_MCI.h
            Driver/Include/Driver_Common.h
    )

    mcux_add_include(
        INCLUDES
            Driver/Include
    )

endif()

if (CONFIG_MCUX_COMPONENT_CMSIS_Driver_Include.NAND)
    mcux_add_source(
        SOURCES
            Driver/Include/Driver_NAND.h
            Driver/Include/Driver_Common.h
    )

    mcux_add_include(
        INCLUDES
            Driver/Include
    )

endif()

if (CONFIG_MCUX_COMPONENT_CMSIS_Driver_Include.SAI)
    mcux_add_source(
        SOURCES
            Driver/Include/Driver_SAI.h
            Driver/Include/Driver_Common.h
    )

    mcux_add_include(
        INCLUDES
            Driver/Include
    )

endif()

if (CONFIG_MCUX_COMPONENT_CMSIS_Driver_Include.SPI)
    mcux_add_source(
        SOURCES
            Driver/Include/Driver_SPI.h
            Driver/Include/Driver_Common.h
    )

    mcux_add_include(
        INCLUDES
            Driver/Include
    )

endif()

if (CONFIG_MCUX_COMPONENT_CMSIS_Driver_Include.USB_Device)
    mcux_add_source(
        SOURCES
            Driver/Include/Driver_USBD.h
            Driver/Include/Driver_USB.h
            Driver/Include/Driver_Common.h
    )

    mcux_add_include(
        INCLUDES
            Driver/Include
    )

endif()

if (CONFIG_MCUX_COMPONENT_CMSIS_Driver_Include.USB_Host)
    mcux_add_source(
        SOURCES
            Driver/Include/Driver_USBH.h
            Driver/Include/Driver_USB.h
            Driver/Include/Driver_Common.h
    )

    mcux_add_include(
        INCLUDES
            Driver/Include
    )

endif()

if (CONFIG_MCUX_COMPONENT_CMSIS_Driver_Include.WiFi)
    mcux_add_source(
        SOURCES
            Driver/Include/Driver_WiFi.h
            Driver/Include/Driver_Common.h
    )

    mcux_add_include(
        INCLUDES
            Driver/Include
    )

endif()

if (CONFIG_MCUX_COMPONENT_CMSIS_Device_API_OSTick)
    mcux_add_source(
        SOURCES
            RTOS2/Include/os_tick.h
    )

    mcux_add_include(
        INCLUDES
            RTOS2/Include/./
    )

endif()

if (CONFIG_MCUX_COMPONENT_CMSIS_Device_API_RTOS2)
    mcux_add_source(
        SOURCES
            RTOS2/Include/cmsis_os2.h
    )

    mcux_add_include(
        INCLUDES
            RTOS2/Include/./
    )

endif()

if (CONFIG_MCUX_COMPONENT_CMSIS_RTOS2_RTX)
    mcux_add_macro(
        CC "-DCMSIS_device_header=\\\"fsl_device_registers.h\\\" -DRTE_COMPONENTS_H"
    )

    mcux_add_source(
        SOURCES
            RTOS2/RTX/Source/rtx_core_c.h
            RTOS2/RTX/Source/rtx_core_ca.h
            RTOS2/RTX/Source/rtx_core_cm.h
            RTOS2/RTX/Source/rtx_delay.c
            RTOS2/RTX/Source/rtx_evflags.c
            RTOS2/RTX/Source/rtx_evr.c
            RTOS2/RTX/Source/rtx_kernel.c
            RTOS2/RTX/Source/rtx_memory.c
            RTOS2/RTX/Source/rtx_mempool.c
            RTOS2/RTX/Source/rtx_msgqueue.c
            RTOS2/RTX/Source/rtx_mutex.c
            RTOS2/RTX/Source/rtx_semaphore.c
            RTOS2/RTX/Source/rtx_system.c
            RTOS2/RTX/Source/rtx_thread.c
            RTOS2/RTX/Source/rtx_timer.c
            RTOS2/RTX/Source/rtx_lib.c
            RTOS2/RTX/Source/rtx_lib.h
            RTOS2/RTX/Include/rtx_evr.h
            RTOS2/RTX/Include/rtx_os.h
            RTOS2/RTX/Include/rtx_def.h
            RTOS2/RTX/Config/RTX_Config.c
            RTOS2/RTX/Config/RTX_Config.h
    )

    mcux_add_source(
        SOURCES
            RTOS2/Source/os_systick.c
            CORES cm0 cm0p cm3 cm4 cm4f cm7 cm7f cm23 cm33 cm33f
    )

    mcux_add_source(
        SOURCES
            RTOS2/Source/os_tick_gtim.c
            RTOS2/Source/os_tick_ptim.c
            CORES ca7
    )

    mcux_add_source(
        SOURCES
            RTOS2/RTX/Source/GCC/irq_armv6m.S
            TOOLCHAINS mdk armgcc mcux
            CORES cm0 cm0p
    )

    mcux_add_source(
        SOURCES
            RTOS2/RTX/Source/GCC/irq_armv7a.S
            TOOLCHAINS mdk armgcc mcux
            CORES ca7
    )

    mcux_add_source(
        SOURCES
            RTOS2/RTX/Source/GCC/irq_armv7m.S
            TOOLCHAINS mdk armgcc mcux
            CORES cm3 cm4 cm7 cm4f cm7f
    )

    mcux_add_source(
        SOURCES
            RTOS2/RTX/Source/GCC/irq_armv8mbl.S
            TOOLCHAINS mdk armgcc mcux
            CORES cm23
    )

    mcux_add_source(
        SOURCES
            RTOS2/RTX/Source/GCC/irq_armv8mml.S
            TOOLCHAINS mdk armgcc mcux
            CORES cm33 cm33f
    )

    mcux_add_source(
        SOURCES
            RTOS2/RTX/Source/IAR/irq_armv6m.s
            TOOLCHAINS iar
            CORES cm0 cm0p
    )

    mcux_add_source(
        SOURCES
            RTOS2/RTX/Source/IAR/irq_armv7a.s
            TOOLCHAINS iar
            CORES ca7
    )

    mcux_add_source(
        SOURCES
            RTOS2/RTX/Source/IAR/irq_armv7m.s
            TOOLCHAINS iar
            CORES cm3 cm4 cm7 cm4f cm7f
    )

    mcux_add_source(
        SOURCES
            RTOS2/RTX/Source/IAR/irq_armv8mbl.s
            TOOLCHAINS iar
            CORES cm23
    )

    mcux_add_source(
        SOURCES
            RTOS2/RTX/Source/IAR/irq_armv8mml.s
            TOOLCHAINS iar
            CORES cm33 cm33f
    )

    mcux_add_include(
        INCLUDES
            RTOS2/RTX/Include/./
            RTOS2/RTX/Config/./
    )

endif()

if (CONFIG_MCUX_COMPONENT_CMSIS_RTOS2_RTX_LIB)
    mcux_add_mdk_configuration(
        CC "-fno-short-wchar -fno-short-enums"
    )

    mcux_add_source(
        SOURCES
            RTOS2/RTX/Source/rtx_core_c.h
            RTOS2/RTX/Source/rtx_core_ca.h
            RTOS2/RTX/Source/rtx_core_cm.h
            RTOS2/RTX/Source/rtx_lib.h
            RTOS2/RTX/Source/rtx_lib.c
            RTOS2/RTX/Include/rtx_evr.h
            RTOS2/RTX/Include/rtx_os.h
            RTOS2/RTX/Include/rtx_def.h
            RTOS2/RTX/Config/RTX_Config.c
            RTOS2/RTX/Config/RTX_Config.h
    )

    mcux_add_library(
        LIBS RTOS2/RTX/Library/IAR/RTX_V6M.a
        TOOLCHAINS iar
        CORES cm0 cm0p
    )

    mcux_add_library(
        LIBS RTOS2/RTX/Library/IAR/RTX_V7M.a
        TOOLCHAINS iar
        CORES cm3 cm4 cm7
    )

    mcux_add_library(
        LIBS RTOS2/RTX/Library/IAR/RTX_V7MF.a
        TOOLCHAINS iar
        CORES cm4f cm7f
    )

    mcux_add_library(
        LIBS RTOS2/RTX/Library/GCC/libRTX_V6M.a
        TOOLCHAINS armgcc mcux
        CORES cm0 cm0p
    )

    mcux_add_library(
        LIBS RTOS2/RTX/Library/GCC/libRTX_V7M.a
        TOOLCHAINS armgcc mcux
        CORES cm3 cm4 cm7
    )

    mcux_add_library(
        LIBS RTOS2/RTX/Library/GCC/libRTX_V7MF.a
        TOOLCHAINS armgcc mcux
        CORES cm4f cm7f
    )

    mcux_add_library(
        LIBS RTOS2/RTX/Library/ARM/RTX_V6M.lib
        TOOLCHAINS mdk
        CORES cm0 cm0p
    )

    mcux_add_library(
        LIBS RTOS2/RTX/Library/ARM/RTX_V7M.lib
        TOOLCHAINS mdk
        CORES cm3 cm4 cm7
    )

    mcux_add_library(
        LIBS RTOS2/RTX/Library/ARM/RTX_V7MF.lib
        TOOLCHAINS mdk
        CORES cm4f cm7f
    )

    mcux_add_library(
        LIBS RTOS2/RTX/Library/IAR/RTX_V8MB.a
        TOOLCHAINS iar
        CORES cm23
        DSP "NO_DSP"
        FPU "NO_FPU"
        TRUSTZONE "TZ"
    )

    mcux_add_library(
        LIBS RTOS2/RTX/Library/IAR/RTX_V8MM.a
        TOOLCHAINS iar
        CORES cm33 cm33f
        DSP "HAS_DSP"
        FPU "NO_FPU"
        TRUSTZONE "TZ"
    )

    mcux_add_library(
        LIBS RTOS2/RTX/Library/IAR/RTX_V8MBN.a
        TOOLCHAINS iar
        CORES cm23
        DSP "NO_DSP"
        FPU "NO_FPU"
        TRUSTZONE "NO_TZ"
    )

    mcux_add_library(
        LIBS RTOS2/RTX/Library/IAR/RTX_V8MMF.a
        TOOLCHAINS iar
        CORES cm33 cm33f
        DSP "HAS_DSP"
        FPU "SP_FPU" "DP_FPU"
        TRUSTZONE "TZ"
    )

    mcux_add_library(
        LIBS RTOS2/RTX/Library/IAR/RTX_V8MMFN.a
        TOOLCHAINS iar
        CORES cm33 cm33f
        DSP "HAS_DSP"
        FPU "SP_FPU" "DP_FPU"
        TRUSTZONE "NO_TZ"
    )

    mcux_add_library(
        LIBS RTOS2/RTX/Library/IAR/RTX_V8MMN.a
        TOOLCHAINS iar
        CORES cm33 cm33f
        DSP "HAS_DSP"
        FPU "NO_FPU"
        TRUSTZONE "NO_TZ"
    )

    mcux_add_library(
        LIBS RTOS2/RTX/Library/GCC/libRTX_V8MB.a
        COMPILERS gcc
        CORES cm23
        DSP "NO_DSP"
        FPU "NO_FPU"
        TRUSTZONE "TZ"
    )

    mcux_add_library(
        LIBS RTOS2/RTX/Library/GCC/libRTX_V8MM.a
        COMPILERS gcc
        CORES cm33 cm33f
        DSP "HAS_DSP"
        FPU "NO_FPU"
        TRUSTZONE "TZ"
    )

    mcux_add_library(
        LIBS RTOS2/RTX/Library/GCC/libRTX_V8MMF.a
        COMPILERS gcc
        CORES cm33 cm33f
        DSP "HAS_DSP"
        FPU "SP_FPU" "DP_FPU"
        TRUSTZONE "TZ"
    )

    mcux_add_library(
        LIBS RTOS2/RTX/Library/GCC/libRTX_V8MBN.a
        COMPILERS gcc
        CORES cm23
        DSP "NO_DSP"
        FPU "NO_FPU"
        TRUSTZONE "NO_TZ"
    )

    mcux_add_library(
        LIBS RTOS2/RTX/Library/GCC/libRTX_V8MMFN.a
        COMPILERS gcc
        CORES cm33 cm33f
        DSP "HAS_DSP"
        FPU "SP_FPU" "DP_FPU"
        TRUSTZONE "NO_TZ"
    )

    mcux_add_library(
        LIBS RTOS2/RTX/Library/GCC/libRTX_V8MMN.a
        COMPILERS gcc
        CORES cm33 cm33f
        DSP "HAS_DSP"
        FPU "NO_FPU"
        TRUSTZONE "NO_TZ"
    )

    mcux_add_library(
        LIBS RTOS2/RTX/Library/CLANG/libRTX_V8MB.a
        COMPILERS armclang
        CORES cm23
        DSP "NO_DSP"
        FPU "NO_FPU"
        TRUSTZONE "TZ"
    )

    mcux_add_library(
        LIBS RTOS2/RTX/Library/CLANG/libRTX_V8MM.a
        COMPILERS armclang
        CORES cm33 cm33f
        DSP "HAS_DSP"
        FPU "NO_FPU"
        TRUSTZONE "TZ"
    )

    mcux_add_library(
        LIBS RTOS2/RTX/Library/CLANG/libRTX_V8MMF.a
        COMPILERS armclang
        CORES cm33 cm33f
        DSP "HAS_DSP"
        FPU "SP_FPU" "DP_FPU"
        TRUSTZONE "TZ"
    )

    mcux_add_library(
        LIBS RTOS2/RTX/Library/CLANG/libRTX_V8MBN.a
        COMPILERS armclang
        CORES cm23
        DSP "NO_DSP"
        FPU "NO_FPU"
        TRUSTZONE "NO_TZ"
    )

    mcux_add_library(
        LIBS RTOS2/RTX/Library/CLANG/libRTX_V8MMFN.a
        COMPILERS armclang
        CORES cm33 cm33f
        DSP "HAS_DSP"
        FPU "SP_FPU" "DP_FPU"
        TRUSTZONE "NO_TZ"
    )

    mcux_add_library(
        LIBS RTOS2/RTX/Library/CLANG/libRTX_V8MMN.a
        COMPILERS armclang
        CORES cm33 cm33f
        DSP "HAS_DSP"
        FPU "NO_FPU"
        TRUSTZONE "NO_TZ"
    )

    mcux_add_include(
        INCLUDES
            RTOS2/RTX/Source
            RTOS2/RTX/Include
            RTOS2/RTX/Config
    )

endif()
