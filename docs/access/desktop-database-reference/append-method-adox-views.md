---
title: Append, méthode (Vues ADOX)
TOCTitle: Append Method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 106dd9d72cb350422f00da05859bc096cb2b52e9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470822"
---
# <a name="append-method-adox-views"></a>Append, méthode (Vues ADOX)


**S’applique à**: Access 2013 | Office 2013


Crée un objet [View](view-object-adox.md) et l'ajoute à la collection [Views](views-collection-adox.md).

## <a name="syntax"></a>Syntaxe

*Affichages*. Ajouter le*nom*, *commande*

## <a name="parameters"></a>Paramètres

  - *Name*

  - Valeur de type **String** qui spécifie le nom de la vue à créer.

  - *Command*

  - Objet [Command](command-object-ado.md) ADO qui représente la vue à créer.

## <a name="remarks"></a>Notes

Crée une vue dans la source de données avec le nom et les attributs spécifiés dans l'objet **Command**.

Si le texte de commande spécifié par l'utilisateur représente une procédure plutôt qu'une vue, le comportement dépend du fournisseur. La méthode **Append** échoue si le fournisseur ne prend pas en charge les commandes persistantes.


> [!NOTE]
> <P>Lorsque vous utilisez le fournisseur OLE DB pour Microsoft Jet, la méthode <STRONG>Append</STRONG> de collection <STRONG>Views</STRONG> vous autorisera à spécifier une <STRONG>procédure</STRONG> plutôt qu’une <STRONG>vue</STRONG> dans le paramètre de <EM>commande</EM> . L'objet <STRONG>Procedure</STRONG> sera ajouté à la source de données et à la collection <STRONG>Views</STRONG>. Après cet <STRONG>ajout</STRONG> et en cas d'actualisation des collections <STRONG>Procedures</STRONG> et <STRONG>Views</STRONG>, l'objet <STRONG>Procedure</STRONG> ne figurera plus dans la collection <STRONG>Views</STRONG> mais apparaîtra dans la collection <STRONG>Procedures</STRONG>.</P>


