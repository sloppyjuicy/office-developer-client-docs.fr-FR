---
title: Append, méthode (Vues ADOX)
TOCTitle: Append method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ccba425e74321f4ab760e9ddc4a722295290ffd1
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925155"
---
# <a name="append-method-adox-views"></a>Append, méthode (Vues ADOX)


**S’applique à**: Access 2013, Office 2013


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
> Lorsque vous utilisez le fournisseur OLE DB pour Microsoft Jet, la méthode **Append** de collection **Views** vous autorisera à spécifier une **procédure** plutôt qu’une **vue** dans le paramètre de *commande* . L'objet **Procedure** sera ajouté à la source de données et à la collection **Views**. Après cet **ajout** et en cas d'actualisation des collections **Procedures** et **Views**, l'objet **Procedure** ne figurera plus dans la collection **Views** mais apparaîtra dans la collection **Procedures**.


