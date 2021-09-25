---
title: CacheSize, propriété (ADO)
TOCTitle: CacheSize property (ADO)
ms:assetid: 42f86cc0-30dc-669b-9e65-5e7ecd52c4d7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249200(v=office.15)
ms:contentKeyID: 48544491
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 70670156970f8f9a4bb52850623e145a0ee062cd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558701"
---
# <a name="cachesize-property-ado"></a>CacheSize, propriété (ADO)


**S’applique à** : Access 2013, Office 2013

Indique le nombre d'enregistrements dans un objet [Recordset](recordset-object-ado.md), placés dans la mémoire cache locale.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur de type **Long** qui doit être supérieure à 0. La valeur par défaut est 1.

## <a name="remarks"></a>Remarques

Utilisez la propriété **CacheSize** pour contrôler le nombre d'enregistrements à récupérer simultanément à partir du fournisseur pour les insérer dans la mémoire locale. Par exemple, si **CacheSize** a pour valeur 10, après la première ouverture de l'objet **Recordset**, le fournisseur extrait les dix premiers enregistrements pour les insérer dans la mémoire locale. À mesure que vous parcourez l'objet **Recordset**, le fournisseur retourne les données du tampon de mémoire local. Dès que vous avez dépassé le dernier enregistrement du cache, le fournisseur récupère les dix enregistrements suivants de la source de données pour les insérer dans le cache.

> [!NOTE]
> [!REMARQUE] **CacheSize** est basé sur la propriété spécifique au fournisseur, **Maximum Open Rows**, (dans la collection **Properties** de l'objet **Recordset** ). Vous ne pouvez pas affecter à **CacheSize** une valeur supérieure à celle de la propriété **Maximum Open Rows**. Pour modifier le nombre de lignes que le fournisseur peut ouvrir, définissez **Maximum Open Rows**.

La valeur de **CacheSize** peut être ajustée au cours de la durée de vie de l'objet **Recordset**, mais si vous modifiez cette valeur, cela n'affecte que le nombre d'enregistrements présents en mémoire cache après plusieurs extractions successives de la source de données. La seule modification de la valeur de la propriété ne modifie pas le contenu actuel du cache.

Si le nombre d'enregistrements à récupérer est inférieur à la valeur de **CacheSize** spécifiée, le fournisseur retourne les enregistrements restants sans qu'aucune erreur ne se produise.

Vous ne pouvez pas utiliser un paramètre **CacheSize** de valeur zéro. Dans ce cas, une erreur est générée.

Les enregistrements extraits du cache ne reflètent pas les modifications simultanées apportées aux données sources par d'autres utilisateurs. Pour forcer la mise à jour de toutes les données mises en cache, utilisez la méthode [Resync](resync-method-ado.md).

Si **CacheSize** a une valeur supérieure à 1, les méthodes de navigation ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext et MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) peuvent parfois accéder à un enregistrement supprimé, si une suppression a lieu après l’extraction des enregistrements. Après l’extraction initiale, les suppressions suivantes ne sont pas reflétées dans le cache de données tant que vous ne tentez pas d’accéder à une valeur de donnée d’une ligne supprimée. Cependant, si vous attribuez la valeur 1 à **CacheSize**, le problème ne se pose pas puisque les lignes supprimées ne peuvent pas être extraites.

