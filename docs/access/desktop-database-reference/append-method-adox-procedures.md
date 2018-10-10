---
title: Append, méthode (Procédures ADOX)
TOCTitle: Append Method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5c1afc7aeea90fc152df7d8f7b1601bf3753b3a3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469441"
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
> <P>Lorsque vous utilisez le fournisseur OLE DB pour Microsoft Jet, la méthode <STRONG>Append</STRONG> de la collection <STRONG>Procedures</STRONG> vous autorisera à spécifier une <STRONG>vue</STRONG> plutôt qu’une <STRONG>procédure</STRONG> dans le paramètre de <EM>commande</EM> . L'objet <STRONG>View</STRONG> sera ajouté à la source de données et à la collection <STRONG>Procedures</STRONG>. Après cet <STRONG>ajout</STRONG> et en cas d'actualisation des collections <STRONG>Procedures</STRONG> et <STRONG>Views</STRONG>, l'objet <STRONG>View</STRONG> ne figurera plus dans la collection <STRONG>Procedures</STRONG> mais apparaîtra dans la collection <STRONG>Views</STRONG>.</P>


