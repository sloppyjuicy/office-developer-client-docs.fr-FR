---
title: Save, méthode - ActiveX Data Objects (ADO)
TOCTitle: Save Method (ADO)
ms:assetid: 02dab13b-f947-b96d-46ea-0def3ed8f28f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248793(v=office.15)
ms:contentKeyID: 48542968
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1b4e3698043c109a8f0fbf32c5c2b8c8ae20e824
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875980"
---
# <a name="save-method-ado"></a><span data-ttu-id="9e1bd-102">Save, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="9e1bd-102">Save Method (ADO)</span></span>


<span data-ttu-id="9e1bd-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9e1bd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9e1bd-104">Enregistre l'objet [Recordset](recordset-object-ado.md) dans un fichier ou un objet [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="9e1bd-104">Saves the [Recordset](recordset-object-ado.md) in a file or [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e1bd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e1bd-105">Syntax</span></span>

<span data-ttu-id="9e1bd-106">*jeu d’enregistrements*. Enregistrer la*Destination*, *PersistFormat*</span><span class="sxs-lookup"><span data-stu-id="9e1bd-106">*recordset*.Save*Destination*, *PersistFormat*</span></span>

## <a name="parameters"></a><span data-ttu-id="9e1bd-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e1bd-107">Parameters</span></span>

  - <span data-ttu-id="9e1bd-108">*Destination*</span><span class="sxs-lookup"><span data-stu-id="9e1bd-108">*Destination*</span></span>

  - <span data-ttu-id="9e1bd-p101">Facultatif. Valeur de type **Variant** qui représente le nom de chemin d'accès complet du fichier dans lequel l'objet **Recordset** doit être enregistré ou une référence à l'objet **Stream**.</span><span class="sxs-lookup"><span data-stu-id="9e1bd-p101">Optional. A **Variant** that represents the complete path name of the file where the **Recordset** is to be saved, or a reference to a **Stream** object.</span></span>

  - <span data-ttu-id="9e1bd-111">*PersistFormat*</span><span class="sxs-lookup"><span data-stu-id="9e1bd-111">*PersistFormat*</span></span>

  - <span data-ttu-id="9e1bd-p102">Facultatif. Valeur [PersistFormatEnum](persistformatenum.md) qui spécifie le format d'enregistrement de l'objet **Recordset** (XML ou ADTG). La valeur par défaut est **adPersistADTG**.</span><span class="sxs-lookup"><span data-stu-id="9e1bd-p102">Optional. A [PersistFormatEnum](persistformatenum.md) value that specifies the format in which the **Recordset** is to be saved (XML or ADTG). The default value is **adPersistADTG**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e1bd-115">Notes</span><span class="sxs-lookup"><span data-stu-id="9e1bd-115">Remarks</span></span>

<span data-ttu-id="9e1bd-p103">La méthode **Save** peut uniquement être appelée sur un objet **Recordset** ouvert. Utilisez la méthode [Open](open-method-ado-recordset.md) pour restaurer ultérieurement l’objet **Recordset** à partir de *Destination*.</span><span class="sxs-lookup"><span data-stu-id="9e1bd-p103">The **Save** method can only be invoked on an open **Recordset**. Use the [Open](open-method-ado-recordset.md) method to later restore the **Recordset** from *Destination*.</span></span>

<span data-ttu-id="9e1bd-p104">Si la propriété [Filter](filter-property-ado.md) est appliquée pour l'objet **Recordset**, seules les lignes accessibles sous le filtre sont enregistrées. Si l'objet **Recordset** est hiérarchique, l'objet **Recordset** enfant actif et ses enfants sont enregistrés, y compris l'objet **Recordset** parent. Si la méthode **Save** d'un objet **Recordset** enfant est appelée, l'enfant et tous ses enfants sont enregistrés mais pas l'objet parent.</span><span class="sxs-lookup"><span data-stu-id="9e1bd-p104">If the [Filter](filter-property-ado.md) property is in effect for the **Recordset**, then only the rows accessible under the filter are saved. If the **Recordset** is hierarchical, then the current child **Recordset** and its children are saved, including the parent **Recordset**. If the **Save** method of a child **Recordset** is called, the child and all its children are saved, but the parent is not.</span></span>

<span data-ttu-id="9e1bd-p105">La première fois que vous enregistrez le **jeu d’enregistrements**, il n’est pas nécessaire d’indiquer une *destination*. Si vous oubliez la *destination*, un nouveau fichier est créé et nommé selon la valeur de la propriété [Source](source-property-ado-recordset.md) du **jeu d’enregistrements**.</span><span class="sxs-lookup"><span data-stu-id="9e1bd-p105">The first time you save the **Recordset**, it is optional to specify *Destination*. If you omit *Destination*, a new file will be created with a name set to the value of the [Source](source-property-ado-recordset.md) property of the **Recordset**.</span></span>

<span data-ttu-id="9e1bd-123">Omettez la *Destination* lorsque vous appelez ensuite **Enregistrer** après le premier enregistrement, ou une erreur d’exécution se produit.</span><span class="sxs-lookup"><span data-stu-id="9e1bd-123">Omit *Destination* when you subsequently call **Save** after the first save, or a run-time error will occur.</span></span> <span data-ttu-id="9e1bd-124">Si vous appelez ensuite **Enregistrer** avec une nouvelle *Destination*, l' **objet Recordset** est enregistré dans la nouvelle destination.</span><span class="sxs-lookup"><span data-stu-id="9e1bd-124">If you subsequently call **Save** with a new *Destination*, the **Recordset** is saved to the new destination.</span></span> <span data-ttu-id="9e1bd-125">Toutefois, la nouvelle destination et la destination d'origine seront toutes deux ouvertes.</span><span class="sxs-lookup"><span data-stu-id="9e1bd-125">However, the new destination and the original destination will both be open.</span></span>

<span data-ttu-id="9e1bd-p107">Dans la mesure où **Save** ne ferme pas l'objet **Recordset** ni *Destination*, vous pouvez continuer à travailler avec l'objet **Recordset** et enregistrer vos modifications les plus récentes. Le paramètre *Destination* reste ouvert jusqu'à la fermeture de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="9e1bd-p107">**Save** does not close the **Recordset** or *Destination*, so you can continue to work with the **Recordset** and save your most recent changes. *Destination* remains open until the **Recordset** is closed.</span></span>

<span data-ttu-id="9e1bd-p108">Pour des raisons de sécurité, la méthode **Save** autorise uniquement l'utilisation de paramètres de sécurité basse et personnalisée à partir d'un script exécuté par Microsoft Internet Explorer. Pour obtenir une explication plus détaillée des problèmes de sécurité, consultez l'article traitant des problèmes de sécurité ADO et RDS dans Microsoft Internet Explorer, figurant dans la rubrique des articles techniques sur les objets ADO (ActiveX Data Object) dans la base des articles techniques traitant de l'accès aux données.</span><span class="sxs-lookup"><span data-stu-id="9e1bd-p108">For reasons of security, the **Save** method permits only the use of low and custom security settings from a script executed by Microsoft Internet Explorer. For a more detailed explanation of security issues, see "ADO and RDS Security Issues in Microsoft Internet Explorer" under ActiveX Data Objects (ADO) Technical Articles in Microsoft Data Access Technical Articles.</span></span>

<span data-ttu-id="9e1bd-130">Si une méthode **Save** est invoquée alors qu'une opération asynchrone de mise à jour, d'exécution ou d'extraction d'un **jeu d'enregistrements** est en cours, la méthode **Save** attend la fin de l'opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="9e1bd-130">If the **Save** method is called while an asynchronous **Recordset** fetch, execute, or update operation is in progress, then **Save** waits until the asynchronous operation is complete.</span></span>

<span data-ttu-id="9e1bd-p109">Les enregistrements sont enregistrés en commençant par la première ligne de l'objet **Recordset**. Une fois l'exécution de la méthode **Save** terminée, la position de ligne active est déplacée à la première ligne de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="9e1bd-p109">Records are saved beginning with the first row of the **Recordset**. When the **Save** method is finished, the current row position is moved to the first row of the **Recordset**.</span></span>

<span data-ttu-id="9e1bd-p110">Pour obtenir de meilleurs résultats, affectez à la propriété [CursorLocation](cursorlocation-property-ado.md) la valeur **adUseClient** avec la méthode **Save**. Si votre fournisseur ne prend pas en charge toutes les fonctionnalités nécessaires à l'enregistrement des objets **Recordset**, le service de curseur les fournira.</span><span class="sxs-lookup"><span data-stu-id="9e1bd-p110">For best results, set the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient** with **Save**. If your provider does not support all of the functionality necessary to save **Recordset** objects, the Cursor Service will provide that functionality.</span></span>

<span data-ttu-id="9e1bd-p111">Lorsqu'un objet **Recordset** est conservé avec la propriété **CursorLocation** affectée de la valeur **adUseServer**, les fonctionnalités de mise à jour de l'objet **Recordset** sont limitées. En général, seules les mises à jour, les insertions et les suppressions de table unique sont autorisées (selon les fonctionnalités du fournisseur). La méthode [Resync](resync-method-ado.md) n'est pas non plus disponible avec une telle configuration.</span><span class="sxs-lookup"><span data-stu-id="9e1bd-p111">When a **Recordset** is persisted with the **CursorLocation** property set to **adUseServer**, the update capability for the **Recordset** is limited. Typically, only single-table updates, insertions, and deletions are allowed (dependant upon provider functionality). The [Resync](resync-method-ado.md) method is also unavailable in this configuration.</span></span>


> [!NOTE]
> <P><span data-ttu-id="9e1bd-138">[!REMARQUE] L'enregistrement d'un objet <STRONG>Recordset</STRONG> avec des <STRONG>champs</STRONG> de type <STRONG>adVariant</STRONG>, <STRONG>adIDispatch</STRONG> ou <STRONG>adIUnknown</STRONG> n'est pas pris en charge par ADO et peut avoir des résultats imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="9e1bd-138">Saving a <STRONG>Recordset</STRONG> with <STRONG>Fields</STRONG> of type <STRONG>adVariant</STRONG>, <STRONG>adIDispatch</STRONG>, or <STRONG>adIUnknown</STRONG> is not supported by ADO and can cause unpredictable results.</span></span></P>



<span data-ttu-id="9e1bd-139">Seuls les **filtres** sous la forme de chaînes de critères (P.ex \> ' 12/31/1999 ') affectent le contenu du **jeu d’enregistrements**persistant.</span><span class="sxs-lookup"><span data-stu-id="9e1bd-139">Only **Filters** in the form of Criteria Strings (e.g. OrderDate \> '12/31/1999') affect the contents of a persisted **Recordset**.</span></span> <span data-ttu-id="9e1bd-140">Les filtres créés avec un tableau de **signets** ou en utilisant une valeur provenant de **FilterGroupEnum** n’affectent pas le contenu du **jeu d’enregistrements**persistant.</span><span class="sxs-lookup"><span data-stu-id="9e1bd-140">Filters created with an Array of **Bookmarks** or using a value from the **FilterGroupEnum** will not affect the contents of the persisted **Recordset**.</span></span> <span data-ttu-id="9e1bd-141">Ces règles s'appliquent aux **jeux d'enregistrements** créés avec des curseurs côté client ou côté serveur.</span><span class="sxs-lookup"><span data-stu-id="9e1bd-141">These rules apply to **Recordsets** created with either client-side or server-side cursors.</span></span>

<span data-ttu-id="9e1bd-142">Étant donné que le paramètre *Destination* accepte tout objet qui prend en charge l’interface OLE DB IStream, vous pouvez enregistrer un **objet Recordset** directement dans l’objet ASP Response.</span><span class="sxs-lookup"><span data-stu-id="9e1bd-142">Because the *Destination* parameter can accept any object that supports the OLE DB IStream interface, you can save a **Recordset** directly to the ASP Response object.</span></span> <span data-ttu-id="9e1bd-143">Pour plus d'informations, consultez [Scénario de persistance des objets Recordset XML](xml-recordset-persistence-scenario.md).</span><span class="sxs-lookup"><span data-stu-id="9e1bd-143">For more details, please see the [XML Recordset Persistence Scenario](xml-recordset-persistence-scenario.md).</span></span>

<span data-ttu-id="9e1bd-144">Vous pouvez également enregistrer un objet **Recordset** au format XML dans une instance d'un objet DOM MSXML, comme l'illustre le code Visual Basic suivant :</span><span class="sxs-lookup"><span data-stu-id="9e1bd-144">You can also save a **Recordset** in XML format to an instance of an MSXML DOM object, as is shown in the following Visual Basic code:</span></span>


> [!NOTE]
> <P><span data-ttu-id="9e1bd-p114">[!REMARQUE] L'enregistrement des objets <STRONG>Recordset</STRONG> hiérarchiques (formes de données) au format XML est assorti de deux limitations. Vous ne pouvez pas enregistrer au format XML si l'objet <STRONG>Recordset</STRONG> hiérarchique contient des mises à jour en attente et vous ne pouvez pas enregistrer un objet <STRONG>Recordset</STRONG> hiérarchique paramétré.</span><span class="sxs-lookup"><span data-stu-id="9e1bd-p114">Two limitations apply when saving hierarchical <STRONG>Recordsets</STRONG> (data shapes) in XML format. You cannot save into XML if the hierarchical <STRONG>Recordset</STRONG> contains pending updates, and you cannot save a parameterized hierarchical <STRONG>Recordset</STRONG>.</span></span></P>



<span data-ttu-id="9e1bd-p115">Un jeu d'enregistrements enregistré au format XML est enregistré à l'aide du format UTF-8. Lorsque ce type de fichier est chargé dans un flux ADO, l'objet Stream ne tente pas d'ouvrir l'objet Recordset à partir du flux sauf si la propriété Charset du flux a la valeur appropriée pour le format UTF-8.</span><span class="sxs-lookup"><span data-stu-id="9e1bd-p115">A Recordset saved in XML format is saved using UTF-8 format. When such a file is loaded into an ADO Stream, the Stream object will not attempt to open a Recordset from the stream unless the Charset property of the stream is set to the appropriate value for UTF-8 format.</span></span>

