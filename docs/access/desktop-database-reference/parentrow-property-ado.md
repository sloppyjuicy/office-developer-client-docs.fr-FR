---
title: ParentRow, propriété (ADO)
TOCTitle: ParentRow property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 372ae0fb41887a3b4bf7203070530d9e00215ccb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568669"
---
# <a name="parentrow-property-ado"></a>ParentRow, propriété (ADO)

**S’applique à** : Access 2013, Office 2013

Indique que le conteneur d'un objet **Row** OLE DB est un objet **ADORecordConstruction**, ce qui indique que le parent de la ligne devient un objet **Record** ADO.

En écriture seule.

## <a name="syntax"></a>Syntaxe

HRESULT put \_ ParentRow( \[ in \] IUnknown \* pParent);

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*pParent* |Le conteneur d'une ligne.|

## <a name="return-values"></a>Valeurs de retour

Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S \_ OK et E \_ FAIL.

## <a name="applies-to"></a>S’applique à

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

