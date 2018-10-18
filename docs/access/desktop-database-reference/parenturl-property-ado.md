---
<span data-ttu-id="314c8-101"><<<<<<< Titre tête : TOCTitle de la propriété ParentURL (ADO) : propriété ParentURL (ADO) === titre : ParentURL, propriété (ADO) TOCTitle : ParentURL, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="314c8-101"><<<<<<< HEAD title: ParentURL Property (ADO) TOCTitle: ParentURL Property (ADO) ======= title: ParentURL property (ADO) TOCTitle: ParentURL property (ADO)</span></span>
>>>>>>> <span data-ttu-id="314c8-102">Master ms:assetid : ec7ec476-6f9e-8486-fe02-74995975df5c ms:mtpsurl : https://msdn.microsoft.com/library/JJ250200(v=office.15) ms:contentKeyID : ms.date 48548517 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="314c8-102">master ms:assetid: ec7ec476-6f9e-8486-fe02-74995975df5c ms:mtpsurl: https://msdn.microsoft.com/library/JJ250200(v=office.15) ms:contentKeyID: 48548517 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="314c8-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="314c8-103"><<<<<<< HEAD</span></span>
# <a name="parenturl-property-ado"></a><span data-ttu-id="314c8-104">ParentURL, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="314c8-104">ParentURL Property (ADO)</span></span>
=======
# <a name="parenturl-property-ado"></a><span data-ttu-id="314c8-105">ParentURL, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="314c8-105">ParentURL property (ADO)</span></span>
>>>>>>> <span data-ttu-id="314c8-106">master</span><span class="sxs-lookup"><span data-stu-id="314c8-106">master</span></span>

<span data-ttu-id="314c8-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="314c8-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="314c8-108">Indique la chaîne d'URL absolue qui pointe vers l'objet [Record](record-object-ado.md) parent de l'objet **Record** actif.</span><span class="sxs-lookup"><span data-stu-id="314c8-108">Indicates an absolute URL string that points to the parent [Record](record-object-ado.md) of the current **Record** object.</span></span>

<span data-ttu-id="314c8-109"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="314c8-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="314c8-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="314c8-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="314c8-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="314c8-111">Return value</span></span>
>>>>>>> <span data-ttu-id="314c8-112">master</span><span class="sxs-lookup"><span data-stu-id="314c8-112">master</span></span>

<span data-ttu-id="314c8-113">Renvoie une valeur **String** qui indique l'URL de l'objet **Record** parent.</span><span class="sxs-lookup"><span data-stu-id="314c8-113">Returns a **String** value that indicates the URL of the parent **Record**.</span></span>

## <a name="remarks"></a><span data-ttu-id="314c8-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="314c8-114">Remarks</span></span>

<span data-ttu-id="314c8-p101">La propriété **ParentURL** dépend de la source utilisée pour ouvrir l'objet **Record**. Cet objet **Record** peut par exemple être ouvert avec une source contenant le nom du chemin d'accès relatif à un répertoire référencé par la propriété [ActiveConnection](activeconnection-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="314c8-p101">The **ParentURL** property depends upon the source used to open the **Record** object. For example, the **Record** may be opened with a source containing a relative path name of a directory referenced by the [ActiveConnection](activeconnection-property-ado.md) property.</span></span>

<span data-ttu-id="314c8-p102">Supposons que « second » est un sous-dossier de « first ». Ouvrez l'objet **Record** comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="314c8-p102">Suppose "second" is a folder contained under "first". Open the **Record** object with the following:</span></span>

```vb
    record.ActiveConnection = "https://first"
    record.Open "second"
```

<span data-ttu-id="314c8-119">À présent, la valeur de la propriété **ParentURL** est la propriété **ParentURL** devient «https://first», comme **ActiveConnection**.</span><span class="sxs-lookup"><span data-stu-id="314c8-119">Now, the value of the **ParentURL** property is **ParentURL** property is "https://first" , the same as **ActiveConnection**.</span></span>

<span data-ttu-id="314c8-120">La source peut également être une URL absolue, tel que «https://first/second».</span><span class="sxs-lookup"><span data-stu-id="314c8-120">The source may also be an absolute URL such as, "https://first/second" .</span></span> <span data-ttu-id="314c8-121">La propriété **ParentURL** devient alors «https://first», le niveau au-dessus.</span><span class="sxs-lookup"><span data-stu-id="314c8-121">The **ParentURL** property is then "https://first" , the level above .</span></span> <span data-ttu-id="314c8-122">La propriété **ParentURL** devient alors «https://first», le niveau supérieur « seconde ».</span><span class="sxs-lookup"><span data-stu-id="314c8-122">The **ParentURL** property is then "https://first" , the level above "second" .</span></span>

<span data-ttu-id="314c8-123">La valeur de cette propriété peut être nulle si :</span><span class="sxs-lookup"><span data-stu-id="314c8-123">This property may be a null value if:</span></span>

- <span data-ttu-id="314c8-124">L'objet actuel n'a pas de parent ; par exemple si l'objet **Record** est la racine d'un répertoire.</span><span class="sxs-lookup"><span data-stu-id="314c8-124">There is no parent for the current object; for example, if the **Record** object represents the root of a directory.</span></span>

- <span data-ttu-id="314c8-125">L'objet **Record** représente une entité qui ne peut pas être spécifiée avec une URL.</span><span class="sxs-lookup"><span data-stu-id="314c8-125">The **Record** object represents an entity that cannot be specified with a URL.</span></span>

<span data-ttu-id="314c8-126">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="314c8-126">This property is read-only.</span></span>


> [!NOTE]
> - <span data-ttu-id="314c8-p104">[!REMARQUE] Cette propriété n'est prise en charge que par les fournisseurs sources des documents, comme le [Fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md). Pour plus d'informations, voir [Enregistrements et champs spécifiques au fournisseur](records-and-provider-supplied-fields.md).</span><span class="sxs-lookup"><span data-stu-id="314c8-p104">This property is only supported by document source providers, such as the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). For more information, see [Records and Provider-Supplied Fields](records-and-provider-supplied-fields.md).</span></span>
> - <span data-ttu-id="314c8-129">[!REMARQUE] Les URL qui utilisent le schéma http appellent automatiquement le fournisseur Microsoft OLE DB pour la publication Internet.</span><span class="sxs-lookup"><span data-stu-id="314c8-129">URLs using the http scheme will automatically invoke the Microsoft OLE DB Provider for Internet Publishing.</span></span> <span data-ttu-id="314c8-130">Pour plus d'informations, voir [URL relatives et absolues](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="314c8-130">For more information, see [Absolute and Relative URLs](absolute-and-relative-urls.md).</span></span> 
> - <span data-ttu-id="314c8-131">[!REMARQUE] Si l'enregistrement actuel contient un enregistrement de données provenant d'un **Recordset** ADO, l'accès à la propriété **ParentURL** génère une erreur d'exécution, indiquant qu'aucune URL n'est possible.</span><span class="sxs-lookup"><span data-stu-id="314c8-131">If the current record contains a data record from an ADO **Recordset**, accessing the **ParentURL** property causes a run-time error, indicating that no URL is possible.</span></span>


