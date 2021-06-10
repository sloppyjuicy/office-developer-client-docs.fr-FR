---
title: ParentURL, propriété (ADO)
TOCTitle: ParentURL property (ADO)
ms:assetid: ec7ec476-6f9e-8486-fe02-74995975df5c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250200(v=office.15)
ms:contentKeyID: 48548517
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8e3735147f813d904c206910ff319913f056946e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287716"
---
# <a name="parenturl-property-ado"></a><span data-ttu-id="4fd6f-102">ParentURL, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="4fd6f-102">ParentURL property (ADO)</span></span>

<span data-ttu-id="4fd6f-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4fd6f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4fd6f-104">Indique la chaîne d'URL absolue qui pointe vers l'objet [Record](record-object-ado.md) parent de l'objet **Record** actif.</span><span class="sxs-lookup"><span data-stu-id="4fd6f-104">Indicates an absolute URL string that points to the parent [Record](record-object-ado.md) of the current **Record** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="4fd6f-105">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4fd6f-105">Return value</span></span>

<span data-ttu-id="4fd6f-106">Renvoie une valeur **String** qui indique l'URL de l'objet **Record** parent.</span><span class="sxs-lookup"><span data-stu-id="4fd6f-106">Returns a **String** value that indicates the URL of the parent **Record**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fd6f-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="4fd6f-107">Remarks</span></span>

<span data-ttu-id="4fd6f-p101">La propriété **ParentURL** dépend de la source utilisée pour ouvrir l’objet **Record**. Cet objet **Record** peut par exemple être ouvert avec une source contenant le nom du chemin d’accès relatif à un répertoire référencé par la propriété [ActiveConnection](activeconnection-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4fd6f-p101">The **ParentURL** property depends upon the source used to open the **Record** object. For example, the **Record** may be opened with a source containing a relative path name of a directory referenced by the [ActiveConnection](activeconnection-property-ado.md) property.</span></span>

<span data-ttu-id="4fd6f-p102">Supposons que « second » est un sous-dossier de « first ». Ouvrez l'objet **Record** comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="4fd6f-p102">Suppose "second" is a folder contained under "first". Open the **Record** object with the following:</span></span>

```vb
    record.ActiveConnection = "https://first"
    record.Open "second"
```

<span data-ttu-id="4fd6f-112">À présent, la valeur de la **propriété ParentURL** est la **propriété ParentURL** est « " , identique https://first à **ActiveConnection**.</span><span class="sxs-lookup"><span data-stu-id="4fd6f-112">Now, the value of the **ParentURL** property is **ParentURL** property is "https://first" , the same as **ActiveConnection**.</span></span>

<span data-ttu-id="4fd6f-113">La source peut également être une URL absolue telle que « https://first/second ».</span><span class="sxs-lookup"><span data-stu-id="4fd6f-113">The source may also be an absolute URL such as, "https://first/second" .</span></span> <span data-ttu-id="4fd6f-114">La **propriété ParentURL** est alors " https://first , le niveau au-dessus.</span><span class="sxs-lookup"><span data-stu-id="4fd6f-114">The **ParentURL** property is then "https://first" , the level above .</span></span> <span data-ttu-id="4fd6f-115">La **propriété ParentURL** est alors « https://first », le niveau au-dessus de « second ».</span><span class="sxs-lookup"><span data-stu-id="4fd6f-115">The **ParentURL** property is then "https://first" , the level above "second" .</span></span>

<span data-ttu-id="4fd6f-116">La valeur de cette propriété peut être nulle si :</span><span class="sxs-lookup"><span data-stu-id="4fd6f-116">This property may be a null value if:</span></span>

- <span data-ttu-id="4fd6f-117">L'objet actuel n'a pas de parent ; par exemple si l'objet **Record** est la racine d'un répertoire.</span><span class="sxs-lookup"><span data-stu-id="4fd6f-117">There is no parent for the current object; for example, if the **Record** object represents the root of a directory.</span></span>

- <span data-ttu-id="4fd6f-118">L'objet **Record** représente une entité qui ne peut pas être spécifiée avec une URL.</span><span class="sxs-lookup"><span data-stu-id="4fd6f-118">The **Record** object represents an entity that cannot be specified with a URL.</span></span>

<span data-ttu-id="4fd6f-119">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="4fd6f-119">This property is read-only.</span></span>


> [!NOTE]
> - <span data-ttu-id="4fd6f-p104">Cette propriété n’est prise en charge que par les fournisseurs sources des documents, comme le [Fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md). Pour plus d’informations, voir [Enregistrements et champs spécifiques au fournisseur](records-and-provider-supplied-fields.md).</span><span class="sxs-lookup"><span data-stu-id="4fd6f-p104">This property is only supported by document source providers, such as the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). For more information, see [Records and Provider-Supplied Fields](records-and-provider-supplied-fields.md).</span></span>
> - <span data-ttu-id="4fd6f-122">Les URL qui utilisent le schéma http appellent automatiquement le fournisseur Microsoft OLE DB pour la publication Internet.</span><span class="sxs-lookup"><span data-stu-id="4fd6f-122">URLs using the http scheme will automatically invoke the Microsoft OLE DB Provider for Internet Publishing.</span></span> <span data-ttu-id="4fd6f-123">Pour plus d’informations, voir [URL relatives et absolues](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="4fd6f-123">For more information, see [Absolute and Relative URLs](absolute-and-relative-urls.md).</span></span> 
> - <span data-ttu-id="4fd6f-124">Si l'enregistrement actuel contient un enregistrement de données provenant d'un **Recordset** ADO, l'accès à la propriété **ParentURL** génère une erreur d'exécution, indiquant qu'aucune URL n'est possible.</span><span class="sxs-lookup"><span data-stu-id="4fd6f-124">If the current record contains a data record from an ADO **Recordset**, accessing the **ParentURL** property causes a run-time error, indicating that no URL is possible.</span></span>


