---
title: Delete, méthode (collection Fields ADO)
TOCTitle: Delete Method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3dc4d3553113a35fba875c3eb23ec544ea3d6b7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471057"
---
# <a name="delete-method-ado-fields-collection"></a>Delete, méthode (collection Fields ADO)


**S’applique à**: Access 2013 | Office 2013



Supprime un objet de la collection [Fields](fields-collection-ado.md).

## <a name="syntax"></a>Syntaxe

*Champs*. Supprimer le*champ*

## <a name="parameters"></a>Paramètres

  - *Field*

  - **Variant** qui désigne l’objet [Field](field-object-ado.md) à supprimer. Ce paramètre peut être le nom de l’objet **Field** ou la position ordinale de l’objet **Field** lui-même.

## <a name="remarks"></a>Notes

L'appel de la méthode **Fields.Delete** sur un objet [Recordset](recordset-object-ado.md) ouvert provoque un erreur d'exécution.

