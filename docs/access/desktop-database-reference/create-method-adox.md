---
title: Create, méthode (ADOX)
TOCTitle: Create Method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cffaa8fb924d2fd272300c77fc5a9c3dc0b239db
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471896"
---
# <a name="create-method-adox"></a><span data-ttu-id="fcaa1-102">Create, méthode (ADOX)</span><span class="sxs-lookup"><span data-stu-id="fcaa1-102">Create Method (ADOX)</span></span>


<span data-ttu-id="fcaa1-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fcaa1-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="fcaa1-104">Crée un catalogue.</span><span class="sxs-lookup"><span data-stu-id="fcaa1-104">Creates a new catalog.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcaa1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fcaa1-105">Syntax</span></span>

<span data-ttu-id="fcaa1-106">*Catalogue*. Créer*ConnectString*</span><span class="sxs-lookup"><span data-stu-id="fcaa1-106">*Catalog*.Create*ConnectString*</span></span>

## <a name="parameters"></a><span data-ttu-id="fcaa1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fcaa1-107">Parameters</span></span>

  - <span data-ttu-id="fcaa1-108">*ConnectString*</span><span class="sxs-lookup"><span data-stu-id="fcaa1-108">*ConnectString*</span></span>

  - <span data-ttu-id="fcaa1-109">Valeur de type **String** utilisée pour se connecter à la source de données.</span><span class="sxs-lookup"><span data-stu-id="fcaa1-109">A **String** value used to connect to the data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcaa1-110">Notes</span><span class="sxs-lookup"><span data-stu-id="fcaa1-110">Remarks</span></span>

<span data-ttu-id="fcaa1-p101">La méthode **Create** crée et ouvre un nouvel objet ADO [Connection](connection-object-ado.md) à la source de données spécifiée dans le paramètre *ConnectString*. En cas de réussite, le nouvel objet **Connection** est affecté à la propriété [ActiveConnection](activeconnection-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="fcaa1-p101">The **Create** method creates and opens a new ADO [Connection](connection-object-ado.md) to the data source specified in *ConnectString*. If successful, the new **Connection** object is assigned to the [ActiveConnection](activeconnection-property-adox.md) property.</span></span>

<span data-ttu-id="fcaa1-113">Une erreur se produit si le fournisseur ne prend pas en charge la création de catalogues.</span><span class="sxs-lookup"><span data-stu-id="fcaa1-113">An error will occur if the provider does not support creating new catalogs.</span></span>

