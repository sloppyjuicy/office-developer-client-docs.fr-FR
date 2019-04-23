---
title: Fournisseur de persistance Microsoft OLE DB (fournisseur de service ADO)
TOCTitle: Microsoft OLE DB Persistence Provider (ADO Service Provider)
ms:assetid: 22e41769-36eb-5a88-05ed-870938657624
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249007(v=office.15)
ms:contentKeyID: 48543719
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4045445120d42f1ca88fce22ce566fc970fce28b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288952"
---
# <a name="microsoft-ole-db-persistence-provider-ado-service-provider"></a><span data-ttu-id="b2f8b-102">Fournisseur de persistance Microsoft OLE DB (fournisseur de services ADO)</span><span class="sxs-lookup"><span data-stu-id="b2f8b-102">Microsoft OLE DB Persistence Provider (ADO Service Provider)</span></span>


<span data-ttu-id="b2f8b-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b2f8b-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="b2f8b-p101">The Microsoft OLE DB Persistence Provider enables you to save a [Recordset](recordset-object-ado.md) object into a file, and later restore that **Recordset** object from the file. Schema information, data, and pending changes are preserved.</span><span class="sxs-lookup"><span data-stu-id="b2f8b-p101">The Microsoft OLE DB Persistence Provider enables you to save a [Recordset](recordset-object-ado.md) object into a file, and later restore that **Recordset** object from the file. Schema information, data, and pending changes are preserved.</span></span>

<span data-ttu-id="b2f8b-106">Vous pouvez enregistrer le **Recordset** au format ADTG (Advanced Data Table Gram) ou au format XML ouvert (Extensible Markup Language).</span><span class="sxs-lookup"><span data-stu-id="b2f8b-106">You can save the **Recordset** in either the proprietary Advanced Data Table Gram (ADTG) format, or the open Extensible Markup Language (XML) format.</span></span>

## <a name="provider-keyword"></a><span data-ttu-id="b2f8b-107">Mot clé du fournisseur</span><span class="sxs-lookup"><span data-stu-id="b2f8b-107">Provider Keyword</span></span>

<span data-ttu-id="b2f8b-108">Pour appeler ce fournisseur, spécifiez le mot clé et la valeur suivants dans la chaîne de connexion.</span><span class="sxs-lookup"><span data-stu-id="b2f8b-108">To invoke this provider, specify the following keyword and value in the connection string.</span></span>

```vb 
 
"Provider=MSPersist" 
```

## <a name="errors"></a><span data-ttu-id="b2f8b-109">Erreurs</span><span class="sxs-lookup"><span data-stu-id="b2f8b-109">Errors</span></span>

<span data-ttu-id="b2f8b-110">Les erreurs suivantes émises par ce fournisseur peuvent être détectées dans votre application.</span><span class="sxs-lookup"><span data-stu-id="b2f8b-110">The following errors issued by this provider can be detected in your application.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b2f8b-111">Constante</span><span class="sxs-lookup"><span data-stu-id="b2f8b-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="b2f8b-112">Description</span><span class="sxs-lookup"><span data-stu-id="b2f8b-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b2f8b-113">E_BADSTREAM</span><span class="sxs-lookup"><span data-stu-id="b2f8b-113">E_BADSTREAM</span></span></p></td>
<td><p><span data-ttu-id="b2f8b-114">Le fichier ouvert n'a pas un format valide (c'est-à-dire que son format n'est ni ADTG, ni XML ).</span><span class="sxs-lookup"><span data-stu-id="b2f8b-114">The file opened does not have a valid format (that is, the format is not ADTG or XML).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2f8b-115">E_CANTPERSISTROWSET</span><span class="sxs-lookup"><span data-stu-id="b2f8b-115">E_CANTPERSISTROWSET</span></span></p></td>
<td><p><span data-ttu-id="b2f8b-116">L'objet <strong>Recordset</strong> enregistré présente des caractéristiques qui l'empêchent d'être stocké.</span><span class="sxs-lookup"><span data-stu-id="b2f8b-116">The <strong>Recordset</strong> object saved has characteristics that prevent it from being stored.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b2f8b-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="b2f8b-117">Remarks</span></span>

<span data-ttu-id="b2f8b-118">Le fournisseur de persistance Microsoft OLE DB n’expose pas de propriétés dynamiques.</span><span class="sxs-lookup"><span data-stu-id="b2f8b-118">The Microsoft OLE DB Persistence Provider exposes no dynamic properties.</span></span>

<span data-ttu-id="b2f8b-119">Actuellement, seuls les objets **Recordset** hiérarchiques paramétrés ne peuvent pas être enregistrés.</span><span class="sxs-lookup"><span data-stu-id="b2f8b-119">Currently, only parameterized hierarchical **Recordset** objects cannot be saved.</span></span>

<span data-ttu-id="b2f8b-120">Pour plus d’informations sur le stockage persistant des objets **Recordset**, consultez la rubrique [Informations complémentaires sur la persistance des objets Recordset](more-about-recordset-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="b2f8b-120">For more information about persistently storing **Recordset** objects, see [Recordset Persistence](more-about-recordset-persistence.md).</span></span>

<span data-ttu-id="b2f8b-121">Lorsqu'un flux est utilisé pour ouvrir un **Recordset**, seul le paramètre *Source* de la méthode **Open** doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="b2f8b-121">When a stream is used to open a **Recordset**, there should be no parameters specified other than the *Source* parameter of the **Open** method.</span></span>

