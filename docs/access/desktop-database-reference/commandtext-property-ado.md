---
title: CommandText, propriété (ADO)
TOCTitle: CommandText Property (ADO)
ms:assetid: 0debec1c-068f-0aea-fce8-e61aa39c5907
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248859(v=office.15)
ms:contentKeyID: 48543234
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231123
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9000f069c7669872c686c013520f886d16e3619b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469134"
---
# <a name="commandtext-property-ado"></a>CommandText, propriété (ADO)


**S’applique à**: Access 2013 | Office 2013

Indique le texte d'une commande à émettre sur un fournisseur.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur de type **String** qui contient une commande de fournisseur, comme une instruction SQL, un nom de table, une URL relative ou un appel de procédure stockée. La valeur par défaut est "" (chaîne de longueur zéro).

## <a name="remarks"></a>Notes

Utilisez la propriété **CommandText** pour définir ou renvoyer le texte d'une commande représentée par un objet [Command](command-object-ado.md). En général, il s'agit d'une instruction SQL, mais il peut également s'agir d'un autre type d'instruction de commande reconnu par le fournisseur, comme un appel de procédure stockée. Le langage, ou la version, utilisé pour une instruction SQL doit être pris en charge par le processeur de requêtes du fournisseur.

Si la propriété [Prepared](prepared-property-ado.md) de l'objet **Command** a la valeur **True** et que l'objet **Command** est lié à une connexion ouverte lorsque vous définissez la propriété **CommandText**, ADO prépare la requête (c'est-à-dire, une forme compilée de la requête, qui est stockée par le fournisseur) lorsque vous appelez les méthodes [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) ou **Open**.

En fonction du paramètre de la propriété [CommandType](commandtype-property-ado.md), ADO peut modifier la propriété **CommandText**. Vous pouvez lire la propriété **CommandText** à tout moment pour découvrir le texte réel de la commande utilisé par ADO au cours de l'exécution.

Utilisez la propriété **CommandText** pour définir ou retourner une URL relative, spécifiant une ressource telle qu'un fichier ou un répertoire. La ressource est relative à un emplacement spécifié explicitement par une URL absolue ou spécifié implicitement par un objet [Connection](connection-object-ado.md) ouvert.


> [!NOTE]
> <P>[!REMARQUE] Les URL utilisant le schéma HTTP appellent automatiquement le <A href="microsoft-ole-db-provider-for-internet-publishing.md">fournisseur Microsoft OLE DB pour la publication Internet</A>. Pour plus d'informations, reportez-vous à la section <A href="absolute-and-relative-urls.md">URL absolues et relatives</A>.</P>


