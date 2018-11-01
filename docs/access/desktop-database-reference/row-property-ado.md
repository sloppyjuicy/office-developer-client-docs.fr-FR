---
title: Row, propriété - ActiveX Data Objects (ADO)
TOCTitle: Row property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7578a00719946450e840080c21284784a27be170
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870946"
---
# <a name="row-property-ado"></a>Row, propriété (ADO)


**S’applique à**: Access 2013, Office 2013



Extrait ou définit un objet **Row** OLE DB à partir de ou sur un objet **ADORecordConstruction**. Lorsque vous utilisez **put\_ligne** pour définir un objet **Row** , une ligne est transformée en objet ADO **Record** . Lecture/écriture.

## <a name="syntax"></a>Syntaxe

Get HRESULT\_ligne (\[out, retval\] IUnknown\* \* ppRow) ;

Placer HRESULT\_ligne (\[dans\] IUnknown\* pRow) ;

## <a name="parameters"></a>Paramètres

  - *ppRow*

  - Pointeur vers un objet **Row** OLE DB.

  - *PRow*

  - Objet **Row** OLE DB.

## <a name="return-values"></a>Valeurs de retour

Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S\_OK et E\_ÉCHOUE.

## <a name="applies-to"></a>Champ d'application

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

