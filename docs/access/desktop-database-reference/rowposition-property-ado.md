---
title: RowPosition, propriété (ADO)
TOCTitle: RowPosition property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6f83d1b113b29be06ffded5263791d3db3068f7f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869070"
---
# <a name="rowposition-property-ado"></a>RowPosition, propriété (ADO)


**S’applique à**: Access 2013, Office 2013



Récupère ou définit un objet **RowPosition** OLE DB à partir de/sur un objet **ADORecordsetConstruction**. Lorsque vous utilisez **put\_RowPosition** pour définir l’objet **RowPosition** , l’objet **Recordset** résultant utilise l’objet **RowPosition** pour déterminer la ligne active.

Lecture/écriture.

## <a name="syntax"></a>Syntaxe

Get HRESULT\_RowPosition (\[out, retval\] IUnknown\* \* ppRowPos) ;

Placer HRESULT\_RowPosition (\[dans\] IUnknown\* pRowPos) ;

## <a name="parameters"></a>Paramètres

  - *ppRowPos*

  - Pointeur vers un objet **RowPosition** OLE DB.

  - *PRowPos*

  - Objet **RowPosition** OLE DB.

## <a name="return-values"></a>Valeurs de retour

Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S\_OK et E\_ÉCHOUE.

## <a name="remarks"></a>Remarques

Lorsque cette propriété est définie, si l’objet **Rowset** de l’objet **RowPosition** est différent de l’objet **Rowset** de l’objet **Recordset** , le premier remplace ce dernier. Le même comportement s’applique au **chapitre** actif à la **RowPosition** .

## <a name="applies-to"></a>Champ d'application

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

