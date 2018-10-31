---
title: Append, méthode (Procédures ADOX)
TOCTitle: Append Method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 195cb08fb0b195b63cdddaa848554f24d028b498
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861875"
---
# <a name="append-method-adox-procedures"></a>Append, méthode (Procédures ADOX)


**S’applique à**: Access 2013 | Office 2013


Ajoute un nouvel objet [Procedure](procedure-object-adox.md) à la collection [Procedures](procedures-collection-adox.md).

## <a name="syntax"></a>Syntaxe

*Procédures*. Ajouter le*nom*, *commande*

## <a name="parameters"></a>Paramètres

  - *Name*

  - Valeur de type **String** qui spécifie le nom de la procédure à créer et à ajouter.

  - *Command*

  - Objet ADO [Command](command-object-ado.md) qui représente la procédure à créer et à ajouter.

## <a name="remarks"></a>Notes

Crée une procédure dans la source de données avec le nom et les attributs spécifiés dans l'objet **Command**.

Si le texte de commande spécifié par l'utilisateur représente une vue plutôt qu'une procédure, le comportement dépend du fournisseur utilisé. La méthode **Append** échoue si le fournisseur ne prend pas en charge les commandes persistantes.


> [!NOTE]
> Lorsque vous utilisez le fournisseur OLE DB pour Microsoft Jet, la méthode **Append** de la collection **Procedures** vous autorisera à spécifier une **vue** plutôt qu’une **procédure** dans le paramètre de *commande* . L'objet **View** sera ajouté à la source de données et à la collection **Procedures**. Après cet **ajout** et en cas d'actualisation des collections **Procedures** et **Views**, l'objet **View** ne figurera plus dans la collection **Procedures** mais apparaîtra dans la collection **Views**.


