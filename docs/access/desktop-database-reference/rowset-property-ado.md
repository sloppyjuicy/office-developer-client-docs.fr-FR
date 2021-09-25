---
title: Rowset, propriété (ADO)
TOCTitle: Rowset property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ad31c4b34f4e94329907264e8ed29eddc08dbecb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615010"
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

