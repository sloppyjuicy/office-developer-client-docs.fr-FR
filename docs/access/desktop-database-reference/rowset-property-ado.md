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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306740"
---
# <a name="rowset-property-ado"></a>Rowset, propriété (ADO)

**S’applique à** : Access 2013, Office 2013

Récupère ou définit un objet **Rowset** OLE DB sur un objet **ADORecordsetConstruction**. Lorsque vous utilisez \_ rowset, le jeu de lignes est transformé en objet **Recordset** ADO.

Lecture-écriture.

## <a name="syntax"></a>Syntaxe

HRESULT get \_ Rowset( \[ out, retval \] IUnknown \* \* ppRowset);

HRESULT put \_ Rowset( \[ in \] IUnknown \* pRowset);

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*ppRowset* |Pointeur vers un objet **Rowset** OLE DB.|
|*PRowset* |Objet **Rowset** OLE DB.|

## <a name="return-values"></a>Valeurs de retour

Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S \_ OK et E \_ FAIL.

## <a name="applies-to"></a>S’applique à

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

