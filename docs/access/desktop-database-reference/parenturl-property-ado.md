---
title: ParentURL, propriété (ADO)
TOCTitle: ParentURL Property (ADO)
ms:assetid: ec7ec476-6f9e-8486-fe02-74995975df5c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250200(v=office.15)
ms:contentKeyID: 48548517
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0fb5e8683bcf7ebe0905b21f169f71834ed424e4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472477"
---
# <a name="parenturl-property-ado"></a><span data-ttu-id="27983-102">ParentURL, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="27983-102">ParentURL Property (ADO)</span></span>

<span data-ttu-id="27983-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="27983-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="27983-104">Indique la chaîne d'URL absolue qui pointe vers l'objet [Record](record-object-ado.md) parent de l'objet **Record** actif.</span><span class="sxs-lookup"><span data-stu-id="27983-104">Indicates an absolute URL string that points to the parent [Record](record-object-ado.md) of the current **Record** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="27983-105">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="27983-105">Return Value</span></span>

<span data-ttu-id="27983-106">Renvoie une valeur **String** qui indique l'URL de l'objet **Record** parent.</span><span class="sxs-lookup"><span data-stu-id="27983-106">Returns a **String** value that indicates the URL of the parent **Record**.</span></span>

## <a name="remarks"></a><span data-ttu-id="27983-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="27983-107">Remarks</span></span>

<span data-ttu-id="27983-p101">La propriété **ParentURL** dépend de la source utilisée pour ouvrir l'objet **Record**. Cet objet **Record** peut par exemple être ouvert avec une source contenant le nom du chemin d'accès relatif à un répertoire référencé par la propriété [ActiveConnection](activeconnection-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="27983-p101">The **ParentURL** property depends upon the source used to open the **Record** object. For example, the **Record** may be opened with a source containing a relative path name of a directory referenced by the [ActiveConnection](activeconnection-property-ado.md) property.</span></span>

<span data-ttu-id="27983-p102">Supposons que « second » est un sous-dossier de « first ». Ouvrez l'objet **Record** comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="27983-p102">Suppose "second" is a folder contained under "first". Open the **Record** object with the following:</span></span>

```vb
    record.ActiveConnection = "https://first"
    record.Open "second"
```

<span data-ttu-id="27983-112">À présent, la valeur de la propriété **ParentURL** est la propriété **ParentURL** devient «https://first», comme **ActiveConnection**.</span><span class="sxs-lookup"><span data-stu-id="27983-112">Now, the value of the **ParentURL** property is **ParentURL** property is "https://first" , the same as **ActiveConnection**.</span></span>

<span data-ttu-id="27983-113">La source peut également être une URL absolue, tel que «https://first/second».</span><span class="sxs-lookup"><span data-stu-id="27983-113">The source may also be an absolute URL such as, "https://first/second" .</span></span> <span data-ttu-id="27983-114">La propriété **ParentURL** devient alors «https://first», le niveau au-dessus.</span><span class="sxs-lookup"><span data-stu-id="27983-114">The **ParentURL** property is then "https://first" , the level above .</span></span> <span data-ttu-id="27983-115">La propriété **ParentURL** devient alors «https://first», le niveau supérieur « seconde ».</span><span class="sxs-lookup"><span data-stu-id="27983-115">The **ParentURL** property is then "https://first" , the level above "second" .</span></span>

<span data-ttu-id="27983-116">La valeur de cette propriété peut être nulle si :</span><span class="sxs-lookup"><span data-stu-id="27983-116">This property may be a null value if:</span></span>

- <span data-ttu-id="27983-117">L'objet actuel n'a pas de parent ; par exemple si l'objet **Record** est la racine d'un répertoire.</span><span class="sxs-lookup"><span data-stu-id="27983-117">There is no parent for the current object; for example, if the **Record** object represents the root of a directory.</span></span>

- <span data-ttu-id="27983-118">L'objet **Record** représente une entité qui ne peut pas être spécifiée avec une URL.</span><span class="sxs-lookup"><span data-stu-id="27983-118">The **Record** object represents an entity that cannot be specified with a URL.</span></span>

<span data-ttu-id="27983-119">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="27983-119">This property is read-only.</span></span>


> [!NOTE]
> - <span data-ttu-id="27983-p104">[!REMARQUE] Cette propriété n'est prise en charge que par les fournisseurs sources des documents, comme le [Fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md). Pour plus d'informations, voir [Enregistrements et champs spécifiques au fournisseur](records-and-provider-supplied-fields.md).</span><span class="sxs-lookup"><span data-stu-id="27983-p104">This property is only supported by document source providers, such as the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). For more information, see [Records and Provider-Supplied Fields](records-and-provider-supplied-fields.md).</span></span>
> - <span data-ttu-id="27983-122">[!REMARQUE] Les URL qui utilisent le schéma http appellent automatiquement le fournisseur Microsoft OLE DB pour la publication Internet.</span><span class="sxs-lookup"><span data-stu-id="27983-122">URLs using the http scheme will automatically invoke the Microsoft OLE DB Provider for Internet Publishing.</span></span> <span data-ttu-id="27983-123">Pour plus d'informations, voir [URL relatives et absolues](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="27983-123">For more information, see [Absolute and Relative URLs](absolute-and-relative-urls.md).</span></span> 
> - <span data-ttu-id="27983-124">[!REMARQUE] Si l'enregistrement actuel contient un enregistrement de données provenant d'un **Recordset** ADO, l'accès à la propriété **ParentURL** génère une erreur d'exécution, indiquant qu'aucune URL n'est possible.</span><span class="sxs-lookup"><span data-stu-id="27983-124">If the current record contains a data record from an ADO **Recordset**, accessing the **ParentURL** property causes a run-time error, indicating that no URL is possible.</span></span>


