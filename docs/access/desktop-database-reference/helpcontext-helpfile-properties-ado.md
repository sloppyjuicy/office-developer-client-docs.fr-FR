---
<span data-ttu-id="78a51-101"><<<<<<< Titre tête : HelpContext, HelpFile propriétés (ADO) TOCTitle : HelpContext, HelpFile propriétés (ADO) ms:assetid : 8a79f994-f17c-2983-0593-095801be762e ms:mtpsurl : https://msdn.microsoft.com/library/JJ249608(v=office.15) ms:contentKeyID : ms.date 48546194 : 09/18 / 2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="78a51-101"><<<<<<< HEAD title: HelpContext, HelpFile Properties (ADO) TOCTitle: HelpContext, HelpFile Properties (ADO) ms:assetid: 8a79f994-f17c-2983-0593-095801be762e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15) ms:contentKeyID: 48546194 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

# <a name="helpcontext-helpfile-properties-ado"></a><span data-ttu-id="78a51-102">HelpContext, HelpFile, propriétés (ADO)</span><span class="sxs-lookup"><span data-stu-id="78a51-102">HelpContext, HelpFile Properties (ADO)</span></span>

<span data-ttu-id="78a51-103">=== titre : HelpContext, HelpFile, propriétés (ADO) TOCTitle : HelpContext, HelpFile propriétés (ADO) ms:assetid : 8a79f994-f17c-2983-0593-095801be762e ms:mtpsurl : https://msdn.microsoft.com/library/JJ249608(v=office.15) ms:contentKeyID : ms.date 48546194 : 17/10/2018 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="78a51-103">======= title: HelpContext, HelpFile properties (ADO) TOCTitle: HelpContext, HelpFile properties (ADO) ms:assetid: 8a79f994-f17c-2983-0593-095801be762e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15) ms:contentKeyID: 48546194 ms.date: 10/17/2018 mtps_version: v=office.15</span></span>
---

# <a name="helpcontext-helpfile-properties-ado"></a><span data-ttu-id="78a51-104">HelpContext, HelpFile, propriétés (ADO)</span><span class="sxs-lookup"><span data-stu-id="78a51-104">HelpContext, HelpFile properties (ADO)</span></span>
>>>>>>> <span data-ttu-id="78a51-105">master</span><span class="sxs-lookup"><span data-stu-id="78a51-105">master</span></span>

<span data-ttu-id="78a51-106">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="78a51-106">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="78a51-107">Indique le fichier d'aide et la rubrique associés à un objet [Error](error-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="78a51-107">Indicates the help file and topic associated with an [Error](error-object-ado.md) object.</span></span>

<span data-ttu-id="78a51-108"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="78a51-108"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="78a51-109">Valeurs renvoyées</span><span class="sxs-lookup"><span data-stu-id="78a51-109">Return Values</span></span>

  - <span data-ttu-id="78a51-110">**HelpContextID**: renvoie un ID de contexte pour une rubrique de fichier d'aide sous forme de valeur **Long**.</span><span class="sxs-lookup"><span data-stu-id="78a51-110">**HelpContextID** — returns a context ID, as a **Long** value, for a topic in a Help file.</span></span>

  - <span data-ttu-id="78a51-111">**HelpFile**: renvoie une valeur **String** qui correspond à un chemin d'accès à un fichier d'aide entièrement résolu.</span><span class="sxs-lookup"><span data-stu-id="78a51-111">**HelpFile** — returns a **String** value that evaluates to a fully resolved path to a Help file.</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="78a51-112">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="78a51-112">Return values</span></span>

- <span data-ttu-id="78a51-113">**HelpContextID**: renvoie un ID de contexte pour une rubrique de fichier d'aide sous forme de valeur **Long**.</span><span class="sxs-lookup"><span data-stu-id="78a51-113">**HelpContextID** — returns a context ID, as a **Long** value, for a topic in a Help file.</span></span>

- <span data-ttu-id="78a51-114">**HelpFile**: renvoie une valeur **String** qui correspond à un chemin d'accès à un fichier d'aide entièrement résolu.</span><span class="sxs-lookup"><span data-stu-id="78a51-114">**HelpFile** — returns a **String** value that evaluates to a fully resolved path to a Help file.</span></span>
>>>>>>> <span data-ttu-id="78a51-115">master</span><span class="sxs-lookup"><span data-stu-id="78a51-115">master</span></span>

## <a name="remarks"></a><span data-ttu-id="78a51-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="78a51-116">Remarks</span></span>

<span data-ttu-id="78a51-p101">Si un fichier d'aide est spécifié dans la propriété **HelpFile**, la propriété **HelpContext** permet d'afficher automatiquement la rubrique d'aide qu'elle identifie. Si aucune rubrique d'aide pertinente n'est disponible, la propriété **HelpContext** renvoie zéro et la propriété **HelpFile** renvoie une chaîne vide (« »).</span><span class="sxs-lookup"><span data-stu-id="78a51-p101">If a Help file is specified in the **HelpFile** property, the **HelpContext** property is used to automatically display the Help topic it identifies. If there is no relevant help topic available, the **HelpContext** property returns zero and the **HelpFile** property returns a zero-length string ("").</span></span>

