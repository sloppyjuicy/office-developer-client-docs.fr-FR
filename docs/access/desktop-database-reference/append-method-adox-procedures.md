---
title: Append, méthode (Procédures ADOX)
TOCTitle: Append method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f086a24ba7069aae02f3001fae9bfe7a360297a9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558988"
---
# <a name="append-method-adox-procedures"></a>Append, méthode (Procédures ADOX)

**S’applique à** : Access 2013, Office 2013

Ajoute un nouvel objet [Procedure](procedure-object-adox.md) à la collection [Procedures](procedures-collection-adox.md).

## <a name="syntax"></a>Syntaxe

*Procédures*. Append *Name*, *Command*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*Name* |Valeur de type **String** qui spécifie le nom de la procédure à créer et à ajouter.|
|*Command* |Objet ADO [Command](command-object-ado.md) qui représente la procédure à créer et à ajouter.|

## <a name="remarks"></a>Remarques

Crée une procédure dans la source de données avec le nom et les attributs spécifiés dans l'objet **Command**.

Si le texte de commande spécifié par l'utilisateur représente une vue plutôt qu'une procédure, le comportement dépend du fournisseur utilisé. La méthode **Append** échoue si le fournisseur ne prend pas en charge les commandes persistantes.

> [!NOTE]
> En cas d'utilisation du fournisseur OLE DB pour Microsoft Jet, la méthode **Append** de la collection **Procedures** vous permet de spécifier un objet **View** plutôt qu'un objet **Procedure** dans le paramètre *Command*. L'objet **View** sera ajouté à la source de données et à la collection **Procedures**. Après cet **ajout** et en cas d'actualisation des collections **Procedures** et **Views**, l'objet **View** ne figurera plus dans la collection **Procedures** mais apparaîtra dans la collection **Views**.


