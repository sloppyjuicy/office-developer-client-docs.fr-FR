---
title: Procedure, objet (ADOX)
TOCTitle: Procedure object (ADOX)
ms:assetid: d5fcf0fe-f59f-e114-dc11-515f11c2a2c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250076(v=office.15)
ms:contentKeyID: 48547972
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ad8f87aa78fbc05694fc53f0d4a55dce43315077
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301392"
---
# <a name="procedure-object-adox"></a><span data-ttu-id="5f566-102">Procedure, objet (ADOX)</span><span class="sxs-lookup"><span data-stu-id="5f566-102">Procedure object (ADOX)</span></span>


<span data-ttu-id="5f566-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5f566-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5f566-p101">Représente une procédure stockée. Utilisé avec l’objet ADO [Command](command-object-ado.md), l’objet **Procedure** permet d’ajouter, de supprimer ou de modifier des procédures stockées.</span><span class="sxs-lookup"><span data-stu-id="5f566-p101">Represents a stored procedure. When used in conjunction with the ADO [Command](command-object-ado.md) object, the **Procedure** object can be used for adding, deleting, or modifying stored procedures.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f566-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="5f566-106">Remarks</span></span>

<span data-ttu-id="5f566-107">L'objet **Procedure** vous permet de créer une procédure stockée sans avoir à connaître ou à utiliser la syntaxe « CREATE PROCEDURE » du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="5f566-107">The **Procedure** object allows you to create a stored procedure without having to know or use the provider's "CREATE PROCEDURE" syntax.</span></span>

<span data-ttu-id="5f566-108">Avec les propriétés d'un objet **Procedure**, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="5f566-108">With the properties of a **Procedure** object, you can:</span></span>

  - <span data-ttu-id="5f566-109">Identifier la procédure à l’aide de la propriété [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="5f566-109">Identify the procedure with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="5f566-110">Spécifier l’objet ADO **Command** à utiliser pour créer ou exécuter la procédure à l’aide de la propriété [Command](command-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="5f566-110">Specify the ADO **Command** object that can be used to create or execute the procedure with the [Command](command-property-adox.md) property.</span></span>

  - <span data-ttu-id="5f566-111">Renvoyer des informations de date à l'aide des propriétés [DateCreated](datecreated-property-adox.md) et [DateModified](datemodified-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="5f566-111">Return date information with the [DateCreated](datecreated-property-adox.md) and [DateModified](datemodified-property-adox.md) properties.</span></span>

