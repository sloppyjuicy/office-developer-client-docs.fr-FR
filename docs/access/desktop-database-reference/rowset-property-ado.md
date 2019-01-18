---
title: Rowset, propriété (ADO)
TOCTitle: Rowset property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: be2a4855b3411a11ddd5a76225acaa52344877a4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706141"
---
# <a name="rowset-property-ado"></a>Rowset, propriété (ADO)

**S’applique à**: Access 2013, Office 2013

Récupère ou définit un objet **Rowset** OLE DB sur un objet **ADORecordsetConstruction**. Lorsque vous utilisez put\_Rowset, l’ensemble de lignes est transformé en un objet **Recordset** .

Lecture-écriture.

## <a name="syntax"></a>Syntaxe

Get HRESULT\_Rowset (\[out, retval\] IUnknown\* \* ppRowset) ;

Placer HRESULT\_Rowset (\[dans\] IUnknown\* pRowset) ;

## <a name="parameters"></a>Parameters

|Paramètre|Description|
|:--------|:----------|
|*ppRowset* |Pointeur vers un objet **Rowset** OLE DB.|
|*PRowset* |Objet **Rowset** OLE DB.|

## <a name="return-values"></a>Valeurs de retour

Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S\_OK et E\_ÉCHOUE.

## <a name="applies-to"></a>S’applique à

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

