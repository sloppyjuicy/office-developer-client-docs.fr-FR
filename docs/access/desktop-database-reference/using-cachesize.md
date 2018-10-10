---
title: À l’aide de la propriété CacheSize (référence de base de données du bureau Access)
TOCTitle: Using CacheSize
ms:assetid: b1677a9f-f22f-9456-0d2a-1ef7cf81bbdf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249846(v=office.15)
ms:contentKeyID: 48547148
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8e4937ee83251f9e4114827860da2ea571887ad8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471124"
---
# <a name="using-cachesize"></a>Utilisation de la propriété CacheSize


**S’applique à**: Access 2013 | Office 2013

Utilisez la propriété **CacheSize** pour contrôler le nombre d'enregistrements à récupérer simultanément à partir du fournisseur pour les insérer dans la mémoire locale. Par exemple, si **CacheSize** a pour valeur 10, après la première ouverture de l'objet **Recordset**, le fournisseur extrait les dix premiers enregistrements pour les insérer dans la mémoire locale. À mesure que vous parcourez l'objet **Recordset**, le fournisseur retourne les données du tampon de mémoire local. Dès que vous avez dépassé le dernier enregistrement du cache, le fournisseur récupère les dix enregistrements suivants de la source de données pour les insérer dans le cache.


> [!NOTE]
> <P>[!REMARQUE] <STRONG>CacheSize</STRONG> dépend de la propriété <STRONG>Maximum Open Rows</STRONG> spécifique au fournisseur (dans la collection <STRONG>Properties</STRONG> de l'objet <STRONG>Recordset</STRONG> ). Vous ne pouvez pas attribuer à <STRONG>CacheSize</STRONG> une valeur supérieure à celle de <STRONG>Maximum Open Rows</STRONG>. Pour modifier le nombre de lignes que le fournisseur peut ouvrir, définissez la valeur de <STRONG>Maximum Open Rows</STRONG>.</P>



La valeur de **CacheSize** peut être modifiée pendant la durée de vie de l'objet **Recordset** mais sa modification affecte uniquement le nombre d'enregistrements dans le cache après des extractions successives de la source des données. La modification de la seule valeur de la propriété ne suffira pas à modifier le contenu actuel du cache.

S'il y a moins d'enregistrements à récupérer que ne l'indique la propriété **CacheSize**, le fournisseur renvoie les enregistrements restants et aucune erreur n'est générée.

L'affectation de la valeur zéro à **CacheSize** est interdite et se traduit par une erreur.

Les enregistrements extraits du cache ne reflètent pas les modifications apportées simultanément par d'autres utilisateurs aux données source. Pour forcer une mise à jour de toutes les données mises en cache, utilisez la méthode [Resync ](resync-method-ado.md).

Si  **CacheSize ** a une valeur supérieure à 1, les méthodes de navigation ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext et MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) risquent d’accéder à un enregistrement supprimé si la suppression a lieu après la récupération des enregistrements. Après l’extraction initiale, les suppressions suivantes ne sont pas répercutées dans votre cache de données tant que vous n’avez pas tenté d’accéder à une valeur de données d’une ligne supprimée. Toutefois, ce problème est résolu si vous affectez la valeur 1 à **CacheSize ** car les lignes supprimées ne peuvent pas être extraites.

