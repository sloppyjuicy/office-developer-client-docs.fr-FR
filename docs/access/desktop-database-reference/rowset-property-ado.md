---
title: Rowset, propriété (ADO)
TOCTitle: Rowset Property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 95a33fb3d24e5cdbf608d268781be0dd536fa315
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470798"
---
# <a name="rowset-property-ado"></a>Rowset, propriété (ADO)


**S’applique à**: Access 2013 | Office 2013



Récupère ou définit un objet **Rowset** OLE DB sur un objet **ADORecordsetConstruction**. Lorsque vous utilisez put\_Rowset, l’ensemble de lignes est transformé en un objet **Recordset** .

Lecture/écriture.

## <a name="syntax"></a>Syntaxe

Get HRESULT\_Rowset (\[out, retval\] IUnknown\* \* ppRowset) ;

Placer HRESULT\_Rowset (\[dans\] IUnknown\* pRowset) ;

## <a name="parameters"></a>Paramètres

  - *ppRowset*

  - Pointeur vers un objet **Rowset** OLE DB.

  - *PRowset*

  - Objet **Rowset** OLE DB.

## <a name="return-values"></a>Valeurs renvoyées

Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S\_OK et E\_ÉCHOUE.

## <a name="applies-to"></a>Champ d'application

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

