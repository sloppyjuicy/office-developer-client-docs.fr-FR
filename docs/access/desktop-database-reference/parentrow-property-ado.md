---
title: ParentRow,, propriété (ADO)
TOCTitle: ParentRow property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2844f7c93164c4b384a895cd32a13bd682154ce3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287737"
---
# <a name="parentrow-property-ado"></a>ParentRow,, propriété (ADO)

**S’applique à** : Access 2013, Office 2013

Indique que le conteneur d'un objet **Row** OLE DB est un objet **ADORecordConstruction**, ce qui indique que le parent de la ligne devient un objet **Record** ADO.

En écriture seule.

## <a name="syntax"></a>Syntaxe

HRESULT put\_parentRow, (\[dans\] IUnknown\* pParent);

## <a name="parameters"></a>Paramètres

|Parameter|Description|
|:--------|:----------|
|*pParent* |Le conteneur d'une ligne.|

## <a name="return-values"></a>Valeurs de retour

Cette méthode de propriété renvoie les valeurs HRESULT standard, y\_compris S OK\_et E Fail.

## <a name="applies-to"></a>S’applique à

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

