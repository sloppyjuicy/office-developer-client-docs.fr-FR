---
title: RowPosition, propriété (ADO)
TOCTitle: RowPosition property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 26ef8dc573e548dbdb2d35d53bd470df63ce17f9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615038"
---
# <a name="rowposition-property-ado"></a>RowPosition, propriété (ADO)

**S’applique à** : Access 2013, Office 2013

Récupère ou définit un objet **RowPosition** OLE DB à partir de/sur un objet **ADORecordsetConstruction**. Lorsque vous utilisez **la valeur \_ RowPosition** pour définir l’objet **RowPosition,** l’objet **Recordset** qui en résulte utilise l’objet **RowPosition** pour déterminer la ligne en cours.

Lecture-écriture.

## <a name="syntax"></a>Syntaxe

HRESULT get \_ RowPosition( \[ out, retval \] IUnknown \* \* ppRowPos);

HRESULT put \_ RowPosition( \[ in \] IUnknown \* pRowPos);

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*ppRowPos* |Pointeur vers un objet **RowPosition** OLE DB.|
|*PRowPos* |Objet **RowPosition** OLE DB.|

## <a name="return-values"></a>Valeurs de retour

Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S \_ OK et E \_ FAIL.

## <a name="remarks"></a>Remarques

When this property is set, if the **Rowset** object on the **RowPosition** object is different from the **Rowset** object on the **Recordset** object, the former overrides the latter. The same behavior applies to the current **Chapter** of the **RowPosition** as well.

## <a name="applies-to"></a>S’applique à

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

