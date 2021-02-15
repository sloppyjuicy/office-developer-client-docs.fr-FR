---
title: Row, propriété - ActiveX Data Objects (ADO)
TOCTitle: Row property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b4beaa742bfc46ecd32fc04733c3e6ddaf12aa2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306481"
---
# <a name="row-property-ado"></a>Row, propriété (ADO)

**S’applique à** : Access 2013, Office 2013

Extrait ou définit un objet **Row** OLE DB à partir de ou sur un objet **ADORecordConstruction**. Lorsque vous utilisez **put \_ Row** pour définir un objet **Row,** une ligne est transformée en objet **Record** ADO. Lecture-écriture.

## <a name="syntax"></a>Syntaxe

HRESULT get \_ Row( \[ out, retval \] IUnknown \* \* ppRow);

HRESULT put \_ Row( \[ in \] IUnknown \* pRow);

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*ppRow* |Pointeur vers un objet **Row** OLE DB.|
|*PRow* |Objet **Row** OLE DB.|

## <a name="return-values"></a>Valeurs de retour

Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S \_ OK et E \_ FAIL.

## <a name="applies-to"></a>S’applique à

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

