---
title: Delete, méthode (collection Fields ADO)
TOCTitle: Delete Method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0fc2e614916026effe6ee0a9766e0b23db200574
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886395"
---
# <a name="delete-method-ado-fields-collection"></a>Delete, méthode (collection Fields ADO)


**S’applique à**: Access 2013, Office 2013



Supprime un objet de la collection [Fields](fields-collection-ado.md).

## <a name="syntax"></a>Syntaxe

*Champs*. Supprimer le*champ*

## <a name="parameters"></a>Paramètres

  - *Field*

  - **Variant** qui désigne l’objet [Field](field-object-ado.md) à supprimer. Ce paramètre peut être le nom de l’objet **Field** ou la position ordinale de l’objet **Field** lui-même.

## <a name="remarks"></a>Notes

L'appel de la méthode **Fields.Delete** sur un objet [Recordset](recordset-object-ado.md) ouvert provoque un erreur d'exécution.

