---
title: Chapter, propriété (ADO)
TOCTitle: Chapter property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1732e32e784f84ab6b21855f94c5b326420cfe41
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618510"
---
# <a name="chapter-property-ado"></a>Chapter, propriété (ADO)

**S’applique à** : Access 2013, Office 2013
 
Extrait ou définit un objet **Chapter** OLE DB à partir de ou sur un objet **ADORecordsetConstruction**. Lorsque vous utilisez **la section \_ « Chapter** » pour définir l’objet **Chapter,** un sous-ensemble de lignes est transformé en objet **Recordset** ADO. Cette opération définit le chapitre actif de l'objet **Rowset**. En lecture/écriture.

## <a name="syntax"></a>Syntaxe

HRESULT get \_ Chapter( \[ out, retval \] long \* plChapter);

HRESULT put \_ Chapter( \[ in long \] lChapter);

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*plChapter* |Pointeur vers le descripteur d'un chapitre.|
|*LChapter* |Descripteur d'un chapitre.|

## <a name="return-values"></a>Valeurs de retour

Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S \_ OK et E \_ FAIL.

## <a name="applies-to"></a>Champ d'application

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

