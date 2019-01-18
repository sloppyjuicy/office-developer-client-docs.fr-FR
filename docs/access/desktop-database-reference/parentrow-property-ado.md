---
title: ParentRow, propriété (ADO)
TOCTitle: ParentRow property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2844f7c93164c4b384a895cd32a13bd682154ce3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721723"
---
# <a name="parentrow-property-ado"></a>ParentRow, propriété (ADO)

**S’applique à**: Access 2013, Office 2013

Indique que le conteneur d'un objet **Row** OLE DB est un objet **ADORecordConstruction**, ce qui indique que le parent de la ligne devient un objet **Record** ADO.

En écriture seule.

## <a name="syntax"></a>Syntaxe

Placer HRESULT\_ligne parente (\[dans\] IUnknown\* pParent) ;

## <a name="parameters"></a>Parameters

|Paramètre|Description|
|:--------|:----------|
|*pParent* |Le conteneur d'une ligne.|

## <a name="return-values"></a>Valeurs de retour

Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S\_OK et E\_ÉCHOUE.

## <a name="applies-to"></a>S’applique à

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

