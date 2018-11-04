---
title: ParentRow, propriété (ADO)
TOCTitle: ParentRow property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 06bb1110dfa7e7a055fa6cd863dcd2cc17f3f585
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950147"
---
# <a name="parentrow-property-ado"></a>ParentRow, propriété (ADO)

**S’applique à**: Access 2013, Office 2013

Indique que le conteneur d'un objet **Row** OLE DB est un objet **ADORecordConstruction**, ce qui indique que le parent de la ligne devient un objet **Record** ADO.

En écriture seule.

## <a name="syntax"></a>Syntaxe

Placer HRESULT\_ligne parente (\[dans\] IUnknown\* pParent) ;

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*pParent* |Le conteneur d'une ligne.|

## <a name="return-values"></a>Valeurs de retour

Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S\_OK et E\_ÉCHOUE.

## <a name="applies-to"></a>S’applique à

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

