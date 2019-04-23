---
title: Open, méthode (enregistrement ADO)
TOCTitle: Open method (ADO Record)
ms:assetid: ba71c5c7-326e-d3b6-0e74-e8343ee6896f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249896(v=office.15)
ms:contentKeyID: 48547371
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: db8953cafc5ad266c81c51e59cbf92787d07cdfb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288377"
---
# <a name="open-method-ado-record"></a><span data-ttu-id="502c4-102">Open, méthode (enregistrement ADO)</span><span class="sxs-lookup"><span data-stu-id="502c4-102">Open method (ADO Record)</span></span>

<span data-ttu-id="502c4-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="502c4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="502c4-104">Ouvre un objet [Record](record-object-ado.md) existant ou crée un nouvel élément représenté par l’objet **Record** (tel qu’un fichier ou un répertoire).</span><span class="sxs-lookup"><span data-stu-id="502c4-104">Opens an existing [Record](record-object-ado.md) object, or creates a new item represented by the **Record** (such as a file or directory).</span></span>

## <a name="syntax"></a><span data-ttu-id="502c4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="502c4-105">Syntax</span></span>

<span data-ttu-id="502c4-106">Open *source*, *ActiveConnection*, *mode*, *CreateOptions*, *options*, *username*, *Password*</span><span class="sxs-lookup"><span data-stu-id="502c4-106">Open *Source*, *ActiveConnection*, *Mode*, *CreateOptions*, *Options*, *UserName*, *Password*</span></span>

## <a name="parameters"></a><span data-ttu-id="502c4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="502c4-107">Parameters</span></span>

|<span data-ttu-id="502c4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="502c4-108">Parameter</span></span>|<span data-ttu-id="502c4-109">Description</span><span class="sxs-lookup"><span data-stu-id="502c4-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="502c4-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="502c4-110">*Source*</span></span> |<span data-ttu-id="502c4-p101">Facultatif. Valeur de type **Variant** qui peut représenter l'URL de l'entité à représenter par cet objet **Record**, un objet **Command**, un objet [Recordset](recordset-object-ado.md) ouvert ou un autre objet **Record**, une chaîne contenant une instruction SELECT SQL ou un nom de table.</span><span class="sxs-lookup"><span data-stu-id="502c4-p101">Optional. A **Variant** that may represent the URL of the entity to be represented by this **Record** object, a **Command**, an open [Recordset](recordset-object-ado.md) or another **Record** object, a string containing a SQL SELECT statement or a table name.</span></span>|
|<span data-ttu-id="502c4-113">*ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="502c4-113">*ActiveConnection*</span></span> | <span data-ttu-id="502c4-p102">Facultatif. Valeur de type **Variant** qui représente la chaîne de connexion ou l'objet [Connection](connection-object-ado.md) ouvert.</span><span class="sxs-lookup"><span data-stu-id="502c4-p102">Optional. A **Variant** that represents the connect string or open [Connection](connection-object-ado.md) object.</span></span>|
|<span data-ttu-id="502c4-116">*Mode*</span><span class="sxs-lookup"><span data-stu-id="502c4-116">*Mode*</span></span> |<span data-ttu-id="502c4-p103">Facultatif. Valeur [ConnectModeEnum](connectmodeenum.md) dont la valeur par défaut est **adModeUnknown**, qui spécifie le mode d'accès à l'objet **Record** résultant.</span><span class="sxs-lookup"><span data-stu-id="502c4-p103">Optional. A [ConnectModeEnum](connectmodeenum.md) value, whose default value is **adModeUnknown**, that specifies the access mode for the resultant **Record** object.</span></span>|
|<span data-ttu-id="502c4-119">*CreateOptions*</span><span class="sxs-lookup"><span data-stu-id="502c4-119">*CreateOptions*</span></span> |<span data-ttu-id="502c4-p104">Facultatif. Valeur [RecordCreateOptionsEnum](recordcreateoptionsenum.md) dont la valeur par défaut est **adFailIfNotExists**, qui spécifie si un fichier ou un répertoire existant doit être ouvert ou s’il faut créer un nouveau fichier ou répertoire. Si la valeur par défaut est définie, le mode d’accès est obtenu de la propriété [Mode](mode-property-ado.md). Ce paramètre n’est pas pris en compte lorsque le paramètre *Source* ne contient pas d’URL.</span><span class="sxs-lookup"><span data-stu-id="502c4-p104">Optional. A [RecordCreateOptionsEnum](recordcreateoptionsenum.md) value, whose default value is **adFailIfNotExists**, that specifies whether an existing file or directory should be opened, or a new file or directory should be created. If set to the default value, the access mode is obtained from the [Mode](mode-property-ado.md) property. This parameter is ignored when the *Source* parameter doesnt contain a URL.</span></span>|
|<span data-ttu-id="502c4-124">*Options*</span><span class="sxs-lookup"><span data-stu-id="502c4-124">*Options*</span></span> |<span data-ttu-id="502c4-p105">Facultatif. Valeur [RecordOpenOptionsEnum](recordopenoptionsenum.md) dont la valeur par défaut est **adOpenRecordUnspecified**, qui spécifie des options pour ouvrir l'objet **Record**. Il est possible de combiner ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="502c4-p105">Optional. A [RecordOpenOptionsEnum](recordopenoptionsenum.md) value, whose default value is **adOpenRecordUnspecified**, that specifies options for opening the **Record**. These values may be combined.</span></span>|
|<span data-ttu-id="502c4-128">*UserName*</span><span class="sxs-lookup"><span data-stu-id="502c4-128">*UserName*</span></span> |<span data-ttu-id="502c4-129">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="502c4-129">Optional.</span></span> <span data-ttu-id="502c4-130">Valeur de type **String** contenant l'ID utilisateur, qui le cas échéant, autorise l'accès à *Source*.</span><span class="sxs-lookup"><span data-stu-id="502c4-130">A **String** value that contains the user ID that, if needed, authorizes access to *Source*.</span></span>|
|<span data-ttu-id="502c4-131">*Password*</span><span class="sxs-lookup"><span data-stu-id="502c4-131">*Password*</span></span> |<span data-ttu-id="502c4-132">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="502c4-132">Optional.</span></span> <span data-ttu-id="502c4-133">Valeur de type **String** contenant le mot de passe qui, le cas échéant, vérifie le paramètre *NomUtilisateur*.</span><span class="sxs-lookup"><span data-stu-id="502c4-133">A **String** value that contains the password that, if needed, verifies *UserName*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="502c4-134">Remarques</span><span class="sxs-lookup"><span data-stu-id="502c4-134">Remarks</span></span>

<span data-ttu-id="502c4-135">*Source* peut représenter les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="502c4-135">*Source* may be:</span></span>

- <span data-ttu-id="502c4-p108">URL. Si le protocole de l'URL est http, le fournisseur Internet est appelé par défaut. Si l'URL pointe vers un nœud qui contient un script exécutable (tel qu'une page .ASP), un objet **Record** contenant la source au lieu du contenu exécuté est ouvert par défaut. Utilisez l'argument *Options* pour modifier ce comportement.</span><span class="sxs-lookup"><span data-stu-id="502c4-p108">A URL. If the protocol for the URL is http, then the Internet Provider will be invoked by default. If the URL points to a node that contains an executable script (such as an .ASP page), then a **Record** containing the source rather than the executed contents is opened by default. Use the *Options* argument to modify this behavior.</span></span>

- <span data-ttu-id="502c4-p109">Objet **Record**. Un objet **Record** ouvert à partir d'un autre objet **Record** clone l'objet **Record** d'origine.</span><span class="sxs-lookup"><span data-stu-id="502c4-p109">A **Record** object. A **Record** object opened from another **Record** will clone the original **Record** object.</span></span>

- <span data-ttu-id="502c4-p110">Objet **Command**. L'objet **Record** ouvert représente la seule ligne retournée par l'exécution de **Command**. Si les résultats contiennent plusieurs lignes, le contenu de la première est placé dans l'enregistrement et une erreur peut être ajoutée à la collection **Errors**.</span><span class="sxs-lookup"><span data-stu-id="502c4-p110">A **Command** object. The opened **Record** object represents the single row returned by executing the **Command**. If the results contain more than a single row, the contents of the first row are placed in the record and an error may be added to the **Errors** collection.</span></span>

- <span data-ttu-id="502c4-p111">Instruction SELECT SQL. L'objet **Record** ouvert représente la seule ligne retournée par l'exécution du contenu de la chaîne. Si les résultats contiennent plusieurs lignes, le contenu de la première est placé dans l'enregistrement et une erreur peut être ajoutée à la collection **Errors**.</span><span class="sxs-lookup"><span data-stu-id="502c4-p111">A SQL SELECT statement. The opened **Record** object represents the single row returned by executing the contents of the string. If the results contain more than a single row, the contents of the first row are placed in the record and an error may be added to the **Errors** collection.</span></span>

- <span data-ttu-id="502c4-148">Nom de table</span><span class="sxs-lookup"><span data-stu-id="502c4-148">A table name.</span></span>

<span data-ttu-id="502c4-149">Si l'objet **Record** représente une entité à laquelle il n'est pas possible d'accéder avec une URL (par exemple une ligne d'un objet **Recordset** dérivé d'une base de données), les valeurs de la propriété [ParentURL](parenturl-property-ado.md) et du champ accédé avec la constante **adRecordURL** sont NULL.</span><span class="sxs-lookup"><span data-stu-id="502c4-149">If the **Record** object represents an entity that cannot be accessed with a URL (for example, a row of a **Recordset** derived from a database), then the values of both the [ParentURL](parenturl-property-ado.md) property and the field accessed with the **adRecordURL** constant are null.</span></span>

> [!NOTE]
> <span data-ttu-id="502c4-150">[!REMARQUE] Les URL qui utilisent le schéma http appellent automatiquement le [fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="502c4-150">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="502c4-151">Pour plus d'informations, consultez la rubrique [URL absolues et relatives](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="502c4-151">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


