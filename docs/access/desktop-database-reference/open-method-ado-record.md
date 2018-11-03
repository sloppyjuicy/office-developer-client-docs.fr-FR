---
title: Open, méthode (enregistrement ADO)
TOCTitle: Open method (ADO Record)
ms:assetid: ba71c5c7-326e-d3b6-0e74-e8343ee6896f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249896(v=office.15)
ms:contentKeyID: 48547371
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ac6b7a65eba6c5547870aa00b486769adab6aa98
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944605"
---
# <a name="open-method-ado-record"></a><span data-ttu-id="8e4b0-102">Open, méthode (enregistrement ADO)</span><span class="sxs-lookup"><span data-stu-id="8e4b0-102">Open method (ADO Record)</span></span>


<span data-ttu-id="8e4b0-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8e4b0-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="8e4b0-104">Ouvre un objet [Record](record-object-ado.md) existant ou crée un nouvel élément représenté par l'objet **Record** (tel qu'un fichier ou un répertoire).</span><span class="sxs-lookup"><span data-stu-id="8e4b0-104">Opens an existing [Record](record-object-ado.md) object, or creates a new item represented by the **Record** (such as a file or directory).</span></span>

## <a name="syntax"></a><span data-ttu-id="8e4b0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e4b0-105">Syntax</span></span>

<span data-ttu-id="8e4b0-106">Ouvrir la *Source*, *ActiveConnection*, *Mode*, *CreateOptions*, *Options*, *nom d’utilisateur*, *mot de passe*</span><span class="sxs-lookup"><span data-stu-id="8e4b0-106">Open *Source*, *ActiveConnection*, *Mode*, *CreateOptions*, *Options*, *UserName*, *Password*</span></span>

## <a name="parameters"></a><span data-ttu-id="8e4b0-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e4b0-107">Parameters</span></span>

  - <span data-ttu-id="8e4b0-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="8e4b0-108">*Source*</span></span>

  - <span data-ttu-id="8e4b0-p101">Facultatif. Valeur de type **Variant** qui peut représenter l'URL de l'entité à représenter par cet objet **Record**, un objet **Command**, un objet [Recordset](recordset-object-ado.md) ouvert ou un autre objet **Record**, une chaîne contenant une instruction SELECT SQL ou un nom de table.</span><span class="sxs-lookup"><span data-stu-id="8e4b0-p101">Optional. A **Variant** that may represent the URL of the entity to be represented by this **Record** object, a **Command**, an open [Recordset](recordset-object-ado.md) or another **Record** object, a string containing a SQL SELECT statement or a table name.</span></span>

  - <span data-ttu-id="8e4b0-111">*ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="8e4b0-111">*ActiveConnection*</span></span>

  - <span data-ttu-id="8e4b0-p102">Facultatif. Valeur de type **Variant** qui représente la chaîne de connexion ou l'objet [Connection](connection-object-ado.md) ouvert.</span><span class="sxs-lookup"><span data-stu-id="8e4b0-p102">Optional. A **Variant** that represents the connect string or open [Connection](connection-object-ado.md) object.</span></span>

  - <span data-ttu-id="8e4b0-114">*Mode*</span><span class="sxs-lookup"><span data-stu-id="8e4b0-114">*Mode*</span></span>

  - <span data-ttu-id="8e4b0-p103">Facultatif. Valeur [ConnectModeEnum](connectmodeenum.md) dont la valeur par défaut est **adModeUnknown**, qui spécifie le mode d'accès à l'objet **Record** résultant.</span><span class="sxs-lookup"><span data-stu-id="8e4b0-p103">Optional. A [ConnectModeEnum](connectmodeenum.md) value, whose default value is **adModeUnknown**, that specifies the access mode for the resultant **Record** object.</span></span>

  - <span data-ttu-id="8e4b0-117">*CreateOptions*</span><span class="sxs-lookup"><span data-stu-id="8e4b0-117">*CreateOptions*</span></span>

  - <span data-ttu-id="8e4b0-118">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="8e4b0-118">Optional.</span></span> <span data-ttu-id="8e4b0-119">Valeur [RecordCreateOptionsEnum](recordcreateoptionsenum.md) dont la valeur par défaut est **adFailIfNotExists**, qui spécifie si un fichier ou un répertoire existant doit être ouvert ou s'il faut créer un nouveau fichier ou répertoire.</span><span class="sxs-lookup"><span data-stu-id="8e4b0-119">A [RecordCreateOptionsEnum](recordcreateoptionsenum.md) value, whose default value is **adFailIfNotExists**, that specifies whether an existing file or directory should be opened, or a new file or directory should be created.</span></span> <span data-ttu-id="8e4b0-120">Si la valeur par défaut est définie, le mode d'accès est obtenu de la propriété [Mode](mode-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="8e4b0-120">If set to the default value, the access mode is obtained from the [Mode](mode-property-ado.md) property.</span></span> <span data-ttu-id="8e4b0-121">Ce paramètre est ignoré lorsque le paramètre *Source* ne contient pas une URL.</span><span class="sxs-lookup"><span data-stu-id="8e4b0-121">This parameter is ignored when the *Source* parameter doesnt contain a URL.</span></span>

  - <span data-ttu-id="8e4b0-122">*Options*</span><span class="sxs-lookup"><span data-stu-id="8e4b0-122">*Options*</span></span>

  - <span data-ttu-id="8e4b0-p105">Facultatif. Valeur [RecordOpenOptionsEnum](recordopenoptionsenum.md) dont la valeur par défaut est **adOpenRecordUnspecified**, qui spécifie des options pour ouvrir l'objet **Record**. Il est possible de combiner ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="8e4b0-p105">Optional. A [RecordOpenOptionsEnum](recordopenoptionsenum.md) value, whose default value is **adOpenRecordUnspecified**, that specifies options for opening the **Record**. These values may be combined.</span></span>

  - <span data-ttu-id="8e4b0-126">*Nom d’utilisateur*</span><span class="sxs-lookup"><span data-stu-id="8e4b0-126">*UserName*</span></span>

  - <span data-ttu-id="8e4b0-p106">Facultatif. Valeur de type **String** contenant l'ID utilisateur, qui le cas échéant, autorise l'accès à *Source*.</span><span class="sxs-lookup"><span data-stu-id="8e4b0-p106">Optional. A **String** value that contains the user ID that, if needed, authorizes access to *Source*.</span></span>

  - <span data-ttu-id="8e4b0-129">*MotDePasse*</span><span class="sxs-lookup"><span data-stu-id="8e4b0-129">*Password*</span></span>

  - <span data-ttu-id="8e4b0-p107">Facultatif. Valeur de type **String** contenant le mot de passe qui, le cas échéant, vérifie le paramètre *NomUtilisateur*.</span><span class="sxs-lookup"><span data-stu-id="8e4b0-p107">Optional. A **String** value that contains the password that, if needed, verifies *UserName*.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e4b0-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="8e4b0-132">Remarks</span></span>

<span data-ttu-id="8e4b0-133">*Source* peut être :</span><span class="sxs-lookup"><span data-stu-id="8e4b0-133">*Source* may be:</span></span>

  - <span data-ttu-id="8e4b0-134">URL.</span><span class="sxs-lookup"><span data-stu-id="8e4b0-134">A URL.</span></span> <span data-ttu-id="8e4b0-135">Si le protocole de l'URL est http, le fournisseur Internet est appelé par défaut.</span><span class="sxs-lookup"><span data-stu-id="8e4b0-135">If the protocol for the URL is http, then the Internet Provider will be invoked by default.</span></span> <span data-ttu-id="8e4b0-136">Si l'URL pointe vers un nœud qui contient un script exécutable (tel qu'une page .ASP), un objet **Record** contenant la source au lieu du contenu exécuté est ouvert par défaut.</span><span class="sxs-lookup"><span data-stu-id="8e4b0-136">If the URL points to a node that contains an executable script (such as an .ASP page), then a **Record** containing the source rather than the executed contents is opened by default.</span></span> <span data-ttu-id="8e4b0-137">Utilisez l’argument *Options* pour modifier ce comportement.</span><span class="sxs-lookup"><span data-stu-id="8e4b0-137">Use the *Options* argument to modify this behavior.</span></span>

  - <span data-ttu-id="8e4b0-p109">Objet **Record**. Un objet **Record** ouvert à partir d'un autre objet **Record** clone l'objet **Record** d'origine.</span><span class="sxs-lookup"><span data-stu-id="8e4b0-p109">A **Record** object. A **Record** object opened from another **Record** will clone the original **Record** object.</span></span>

  - <span data-ttu-id="8e4b0-p110">Objet **Command**. L'objet **Record** ouvert représente la seule ligne retournée par l'exécution de **Command**. Si les résultats contiennent plusieurs lignes, le contenu de la première est placé dans l'enregistrement et une erreur peut être ajoutée à la collection **Errors**.</span><span class="sxs-lookup"><span data-stu-id="8e4b0-p110">A **Command** object. The opened **Record** object represents the single row returned by executing the **Command**. If the results contain more than a single row, the contents of the first row are placed in the record and an error may be added to the **Errors** collection.</span></span>

  - <span data-ttu-id="8e4b0-p111">Instruction SELECT SQL. L'objet **Record** ouvert représente la seule ligne retournée par l'exécution du contenu de la chaîne. Si les résultats contiennent plusieurs lignes, le contenu de la première est placé dans l'enregistrement et une erreur peut être ajoutée à la collection **Errors**.</span><span class="sxs-lookup"><span data-stu-id="8e4b0-p111">A SQL SELECT statement. The opened **Record** object represents the single row returned by executing the contents of the string. If the results contain more than a single row, the contents of the first row are placed in the record and an error may be added to the **Errors** collection.</span></span>

  - <span data-ttu-id="8e4b0-146">Nom de table</span><span class="sxs-lookup"><span data-stu-id="8e4b0-146">A table name.</span></span>

<span data-ttu-id="8e4b0-147">Si l'objet **Record** représente une entité à laquelle il n'est pas possible d'accéder avec une URL (par exemple une ligne d'un objet **Recordset** dérivé d'une base de données), les valeurs de la propriété [ParentURL](parenturl-property-ado.md) et du champ accédé avec la constante **adRecordURL** sont NULL.</span><span class="sxs-lookup"><span data-stu-id="8e4b0-147">If the **Record** object represents an entity that cannot be accessed with a URL (for example, a row of a **Recordset** derived from a database), then the values of both the [ParentURL](parenturl-property-ado.md) property and the field accessed with the **adRecordURL** constant are null.</span></span>


> [!NOTE]
> <span data-ttu-id="8e4b0-148">[!REMARQUE] Les URL qui utilisent le schéma http appellent automatiquement le [fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="8e4b0-148">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="8e4b0-149">Pour plus d’informations, consultez [URL absolues et relatives](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="8e4b0-149">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


