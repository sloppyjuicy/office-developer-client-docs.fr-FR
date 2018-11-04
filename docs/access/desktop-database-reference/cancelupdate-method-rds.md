---
title: CancelUpdate, méthode (RDS)
TOCTitle: CancelUpdate method (RDS)
ms:assetid: 373a3feb-125d-915a-fd56-d4b04b20db54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249130(v=office.15)
ms:contentKeyID: 48544188
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 794c77c0ab6ab2abf22b04def8763fd1e0c51913
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949613"
---
# <a name="cancelupdate-method-rds"></a>CancelUpdate, méthode (RDS)

**S’applique à**: Access 2013, Office 2013

Annule toutes les modifications apportées à la ligne active ou à une nouvelle ligne d'un objet [Recordset](recordset-object-ado.md).

## <a name="syntax"></a>Syntaxe

*DataControl*. CancelUpdate

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*DataControl* |Une variable objet qui représente un objet [RDS.DataControl](datacontrol-object-rds.md).|

## <a name="remarks"></a>Notes

Le service de curseur pour OLE DB conserve à la fois une copie des valeurs d'origine et un cache des modifications. Lorsque vous appelez la méthode **CancelUpdate**, le cache des modifications est réinitialisé et vidé et tous les contrôles dépendants sont actualisés avec les données d'origine.

