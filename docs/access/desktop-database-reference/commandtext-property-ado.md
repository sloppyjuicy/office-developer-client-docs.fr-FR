---
title: CommandText, propriété (ADO)
TOCTitle: CommandText property (ADO)
ms:assetid: 0debec1c-068f-0aea-fce8-e61aa39c5907
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248859(v=office.15)
ms:contentKeyID: 48543234
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231123
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: c2fd60d7e14b840a11d12069dbd72879167c3bae
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565806"
---
# <a name="commandtext-property-ado"></a>CommandText, propriété (ADO)


**S’applique à** : Access 2013, Office 2013

Indique le texte d'une commande à émettre sur un fournisseur.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur de type **String** qui contient une commande de fournisseur, comme une instruction SQL, un nom de table, une URL relative ou un appel de procédure stockée. La valeur par défaut est "" (chaîne de longueur zéro).

## <a name="remarks"></a>Remarques

Utilisez la propriété **CommandText** pour définir ou renvoyer le texte d'une commande représentée par un objet [Command](command-object-ado.md). En général, il s'agit d'une instruction SQL, mais il peut également s'agir d'un autre type d'instruction de commande reconnu par le fournisseur, comme un appel de procédure stockée. Le langage, ou la version, utilisé pour une instruction SQL doit être pris en charge par le processeur de requêtes du fournisseur.

Si la propriété [Prepared](prepared-property-ado.md) de l'objet **Command** a la valeur **True** et que l'objet **Command** est lié à une connexion ouverte lorsque vous définissez la propriété **CommandText**, ADO prépare la requête (c'est-à-dire, une forme compilée de la requête, qui est stockée par le fournisseur) lorsque vous appelez les méthodes [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) ou **Open**.

En fonction du paramètre de la propriété [CommandType](commandtype-property-ado.md), ADO peut modifier la propriété **CommandText**. Vous pouvez lire la propriété **CommandText** à tout moment pour découvrir le texte réel de la commande utilisé par ADO au cours de l'exécution.

Utilisez la propriété **CommandText** pour définir ou retourner une URL relative, spécifiant une ressource telle qu'un fichier ou un répertoire. La ressource est relative à un emplacement spécifié explicitement par une URL absolue ou spécifié implicitement par un objet [Connection](connection-object-ado.md) ouvert.


> [!NOTE]
> Les URL qui utilisent le schéma http appellent automatiquement le [fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md). Pour plus d’informations, voir [URL absolues et relatives.](absolute-and-relative-urls.md)


