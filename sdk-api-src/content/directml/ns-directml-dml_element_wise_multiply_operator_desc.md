---
UID: NS:directml.DML_ELEMENT_WISE_MULTIPLY_OPERATOR_DESC
title: DML_ELEMENT_WISE_MULTIPLY_OPERATOR_DESC
description: Computes the product of each pair of corresponding elements of the input tensors, placing the result into the corresponding element of *OutputTensor*.
helpviewer_keywords: ["DML_ELEMENT_WISE_MULTIPLY_OPERATOR_DESC","DML_ELEMENT_WISE_MULTIPLY_OPERATOR_DESC structure","direct3d12.dml_element_wise_multiply_operator_desc","directml/DML_ELEMENT_WISE_MULTIPLY_OPERATOR_DESC"]
old-location: direct3d12\dml_element_wise_multiply_operator_desc.htm
tech.root: directml
ms.assetid: 1ACECE42-6B96-487D-998E-DDCD202E8A01
ms.date: 10/30/2020
req.header: directml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DML_ELEMENT_WISE_MULTIPLY_OPERATOR_DESC
 - directml/DML_ELEMENT_WISE_MULTIPLY_OPERATOR_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DirectML.h
api_name:
 - DML_ELEMENT_WISE_MULTIPLY_OPERATOR_DESC
---

## -description

Computes the product of each pair of corresponding elements of the input tensors, placing the result into the corresponding element of *OutputTensor*.

```
f(a, b) = a * b
```

This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.

## -struct-fields

### -field ATensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the left-hand side inputs.

### -field BTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the right-hand side inputs.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The output tensor to write the results to.

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_1_0`.

## Tensor constraints
*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.

## Tensor support
### DML_FEATURE_LEVEL_3_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| ATensor | Input | 1 to 8 | FLOAT32, FLOAT16, INT32, UINT32 |
| BTensor | Input | 1 to 8 | FLOAT32, FLOAT16, INT32, UINT32 |
| OutputTensor | Output | 1 to 8 | FLOAT32, FLOAT16, INT32, UINT32 |

### DML_FEATURE_LEVEL_2_1 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| ATensor | Input | 4 to 5 | FLOAT32, FLOAT16, INT32, UINT32 |
| BTensor | Input | 4 to 5 | FLOAT32, FLOAT16, INT32, UINT32 |
| OutputTensor | Output | 4 to 5 | FLOAT32, FLOAT16, INT32, UINT32 |

### DML_FEATURE_LEVEL_1_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| ATensor | Input | 4 to 5 | FLOAT32, FLOAT16 |
| BTensor | Input | 4 to 5 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 4 to 5 | FLOAT32, FLOAT16 |
