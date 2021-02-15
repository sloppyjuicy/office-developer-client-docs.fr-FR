---
title: View Object (ADOX - Référence de base de données de bureau Access)
TOCTitle: View object (ADOX)
ms:assetid: 3b2e9972-8a0d-eaa3-1c93-ae0665a47f02
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249149(v=office.15)
ms:contentKeyID: 48544280
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b3b5d25a727233b5fda5627df8dff952003bbfe3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306048"
---
# <a name="view-object-adox"></a><span data-ttu-id="cdc87-102">View, objet (ADOX)</span><span class="sxs-lookup"><span data-stu-id="cdc87-102">View object (ADOX)</span></span>


<span data-ttu-id="cdc87-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cdc87-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cdc87-p101">Représente un jeu d'enregistrements filtré ou une table virtuelle. Utilisé avec l'objet ADO [Command](command-object-ado.md), l'objet **View** permet d'ajouter, de supprimer ou de modifier des vues.</span><span class="sxs-lookup"><span data-stu-id="cdc87-p101">Represents a filtered set of records or a virtual table. When used in conjunction with the ADO [Command](command-object-ado.md) object, the **View** object can be used for adding, deleting, or modifying views.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdc87-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="cdc87-106">Remarks</span></span>

<span data-ttu-id="cdc87-p102">Une vue est une table virtuelle créée à partir d'autres tables ou vues de base de données. Les objets **View** vous permettent de créer une vue sans avoir à connaître ou utiliser la syntaxe « CREATE VIEW » du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="cdc87-p102">A view is a virtual table, created from other database tables or views. The **View** object allows you to create a view without having to know or use the provider's "CREATE VIEW" syntax.</span></span>

<span data-ttu-id="cdc87-109">Avec les propriétés d'un objet **View**, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="cdc87-109">With the properties of a **View** object, you can:</span></span>

  - <span data-ttu-id="cdc87-110">Identifier la vue à l'aide de la propriété [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="cdc87-110">Identify the view with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="cdc87-111">Spécifier l'objet ADO **Command** à utiliser pour ajouter, supprimer ou modifier les vues à l'aide de la propriété [Command](command-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="cdc87-111">Specify the ADO **Command** object that can be used to add, delete, or modify views with the [Command](command-property-adox.md) property.</span></span>

  - <span data-ttu-id="cdc87-112">Renvoyer des informations de date à l'aide des propriétés [DateCreated](datecreated-property-adox.md) et [DateModified](datemodified-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="cdc87-112">Return date information with the [DateCreated](datecreated-property-adox.md) and [DateModified](datemodified-property-adox.md) properties.</span></span>

