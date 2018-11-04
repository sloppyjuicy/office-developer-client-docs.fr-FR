---
title: Rowset, propriété (ADO)
TOCTitle: Rowset property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0d5979cb42e2ed4a979dc07016a4bb02b8097994
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949788"
---
# <a name="rowset-property-ado"></a>Rowset, propriété (ADO)

**S’applique à**: Access 2013, Office 2013

Récupère ou définit un objet **Rowset** OLE DB sur un objet **ADORecordsetConstruction**. Lorsque vous utilisez put\_Rowset, l’ensemble de lignes est transformé en un objet **Recordset** .

Lecture/écriture.

## <a name="syntax"></a>Syntaxe

Get HRESULT\_Rowset (\[out, retval\] IUnknown\* \* ppRowset) ;

Placer HRESULT\_Rowset (\[dans\] IUnknown\* pRowset) ;

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*ppRowset* |Pointeur vers un objet **Rowset** OLE DB.|
|*PRowset* |Objet **Rowset** OLE DB.|

## <a name="return-values"></a>Valeurs de retour

Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S\_OK et E\_ÉCHOUE.

## <a name="applies-to"></a>S’applique à

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

