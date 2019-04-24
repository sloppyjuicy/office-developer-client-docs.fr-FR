---
title: RowPosition, propriété (ADO)
TOCTitle: RowPosition property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84d3ad7cc5b3d43b15ac1113f6fa00932678ebc3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306859"
---
# <a name="rowposition-property-ado"></a>RowPosition, propriété (ADO)

**S’applique à** : Access 2013, Office 2013

Récupère ou définit un objet **RowPosition** OLE DB à partir de/sur un objet **ADORecordsetConstruction**. Lorsque vous utilisez **put\_RowPosition** pour définir l'objet **RowPosition** , l'objet **Recordset** résultant utilise l'objet **RowPosition** pour déterminer la ligne active.

Lecture-écriture.

## <a name="syntax"></a>Syntaxe

HRESULT get\_RowPosition (\[out, retval\] IUnknown\* \* ppRowPos);

HRESULT put\_RowPosition (\[dans\] IUnknown\* pRowPos);

## <a name="parameters"></a>Paramètres

|Parameter|Description|
|:--------|:----------|
|*ppRowPos* |Pointeur vers un objet **RowPosition** OLE DB.|
|*PRowPos* |Objet **RowPosition** OLE DB.|

## <a name="return-values"></a>Valeurs de retour

Cette méthode de propriété renvoie les valeurs HRESULT standard, y\_compris S OK\_et E Fail.

## <a name="remarks"></a>Remarques

When this property is set, if the **Rowset** object on the **RowPosition** object is different from the **Rowset** object on the **Recordset** object, the former overrides the latter. The same behavior applies to the current **Chapter** of the **RowPosition** as well.

## <a name="applies-to"></a>S’applique à

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

