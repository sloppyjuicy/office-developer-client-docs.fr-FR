---
title: Procedure, objet (ADOX)
TOCTitle: Procedure Object (ADOX)
ms:assetid: d5fcf0fe-f59f-e114-dc11-515f11c2a2c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250076(v=office.15)
ms:contentKeyID: 48547972
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: afc4eae76395e7a15573ad5343955b0ab46df3db
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883350"
---
# <a name="procedure-object-adox"></a><span data-ttu-id="e7453-102">Procedure, objet (ADOX)</span><span class="sxs-lookup"><span data-stu-id="e7453-102">Procedure Object (ADOX)</span></span>


<span data-ttu-id="e7453-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e7453-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e7453-p101">Représente une procédure stockée. Utilisé avec l'objet ADO [Command](command-object-ado.md), l'objet **Procedure** permet d'ajouter, de supprimer ou de modifier des procédures stockées.</span><span class="sxs-lookup"><span data-stu-id="e7453-p101">Represents a stored procedure. When used in conjunction with the ADO [Command](command-object-ado.md) object, the **Procedure** object can be used for adding, deleting, or modifying stored procedures.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7453-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="e7453-106">Remarks</span></span>

<span data-ttu-id="e7453-107">L'objet **Procedure** vous permet de créer une procédure stockée sans avoir à connaître ou à utiliser la syntaxe « CREATE PROCEDURE » du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="e7453-107">The **Procedure** object allows you to create a stored procedure without having to know or use the provider's "CREATE PROCEDURE" syntax.</span></span>

<span data-ttu-id="e7453-108">Avec les propriétés d'un objet **Procedure**, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="e7453-108">With the properties of a **Procedure** object, you can:</span></span>

  - <span data-ttu-id="e7453-109">Identifier la procédure à l'aide de la propriété [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="e7453-109">Identify the procedure with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="e7453-110">Spécifier l'objet ADO **Command** à utiliser pour créer ou exécuter la procédure à l'aide de la propriété [Command](command-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="e7453-110">Specify the ADO **Command** object that can be used to create or execute the procedure with the [Command](command-property-adox.md) property.</span></span>

  - <span data-ttu-id="e7453-111">Renvoyer des informations de date à l'aide des propriétés [DateCreated](datecreated-property-adox.md) et [DateModified](datemodified-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="e7453-111">Return date information with the [DateCreated](datecreated-property-adox.md) and [DateModified](datemodified-property-adox.md) properties.</span></span>

