---
title: ParentRow, propriété (ADO)
TOCTitle: ParentRow Property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 834dcaed7d1acdcf66410584436e2ccee8c91c56
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472565"
---
# <a name="parentrow-property-ado"></a>ParentRow, propriété (ADO)


**S’applique à**: Access 2013 | Office 2013


Indique que le conteneur d'un objet **Row** OLE DB est un objet **ADORecordConstruction**, ce qui indique que le parent de la ligne devient un objet **Record** ADO.

En écriture seule.

## <a name="syntax"></a>Syntaxe

Placer HRESULT\_ligne parente (\[dans\] IUnknown\* pParent) ;

## <a name="parameters"></a>Paramètres

  - *pParent*

  - Le conteneur d'une ligne.

## <a name="return-values"></a>Valeurs renvoyées

Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S\_OK et E\_ÉCHOUE.

## <a name="applies-to"></a>Champ d'application

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

