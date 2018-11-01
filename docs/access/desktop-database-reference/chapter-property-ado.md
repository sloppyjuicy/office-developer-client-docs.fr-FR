---
title: Chapter, propriété (ADO)
TOCTitle: Chapter property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5eeb3c6e2e8c7b7f1c0f6e733c1b86545a5e954f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887823"
---
# <a name="chapter-property-ado"></a>Chapter, propriété (ADO)


**S’applique à**: Access 2013, Office 2013
 

Extrait ou définit un objet **Chapter** OLE DB à partir de ou sur un objet **ADORecordsetConstruction**. Lorsque vous utilisez **put\_chapitre** pour définir l’objet **Chapter** , un sous-ensemble de lignes est transformé en un objet **Recordset** . Cette opération définit le chapitre actif de l'objet **Rowset**. En lecture/écriture.

## <a name="syntax"></a>Syntaxe

Get HRESULT\_chapitre (\[out, retval\] long\* plChapter) ;

Placer HRESULT\_chapitre (\[dans\] lChapter long) ;

## <a name="parameters"></a>Paramètres

  - *plChapter*

  - Pointeur vers le descripteur d'un chapitre.

  - *LChapter*

  - Descripteur d'un chapitre.

## <a name="return-values"></a>Valeurs de retour

Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S\_OK et E\_ÉCHOUE.

## <a name="applies-to"></a>Champ d'application

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

