---
title: Chapter, propriété (ADO)
TOCTitle: Chapter property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b4f4efc2ffab9f7996b2d805658b985badbaf87e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296394"
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

