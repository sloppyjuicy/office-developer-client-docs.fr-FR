---
<span data-ttu-id="5cd6b-101"><<<<<<< Titre tête : TOCTitle chapitre propriété (ADO) : chapitre propriété (ADO) === titre : Chapter, propriété (ADO) TOCTitle : Chapter, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="5cd6b-101"><<<<<<< HEAD title: Chapter Property (ADO) TOCTitle: Chapter Property (ADO) ======= title: Chapter property (ADO) TOCTitle: Chapter property (ADO)</span></span>
>>>>>>> <span data-ttu-id="5cd6b-102">Master ms:assetid : d7c9478e-487f-7023-1dd8-5313433dbc5e ms:mtpsurl : https://msdn.microsoft.com/library/JJ250085(v=office.15) ms:contentKeyID : ms.date 48548014 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="5cd6b-102">master ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15) ms:contentKeyID: 48548014 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="5cd6b-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="5cd6b-103"><<<<<<< HEAD</span></span>
# <a name="chapter-property-ado"></a><span data-ttu-id="5cd6b-104">Chapter, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="5cd6b-104">Chapter Property (ADO)</span></span>
=======
# <a name="chapter-property-ado"></a><span data-ttu-id="5cd6b-105">Chapter, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="5cd6b-105">Chapter property (ADO)</span></span>
>>>>>>> <span data-ttu-id="5cd6b-106">master</span><span class="sxs-lookup"><span data-stu-id="5cd6b-106">master</span></span>


<span data-ttu-id="5cd6b-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5cd6b-107">**Applies to**: Access 2013 | Office 2013</span></span>
 

<span data-ttu-id="5cd6b-108">Extrait ou définit un objet **Chapter** OLE DB à partir de ou sur un objet **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="5cd6b-108">Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="5cd6b-109">Lorsque vous utilisez **put\_chapitre** pour définir l’objet **Chapter** , un sous-ensemble de lignes est transformé en un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="5cd6b-109">When you use **put\_Chapter** to set the **Chapter** object, a subset of rows is turned into an ADO **Recordset** object.</span></span> <span data-ttu-id="5cd6b-110">Cette opération définit le chapitre actif de l'objet **Rowset**.</span><span class="sxs-lookup"><span data-stu-id="5cd6b-110">This sets the current chapter of the **Rowset** object.</span></span> <span data-ttu-id="5cd6b-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="5cd6b-111">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cd6b-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5cd6b-112">Syntax</span></span>

<span data-ttu-id="5cd6b-113">Get HRESULT\_chapitre (\[out, retval\] long\* plChapter) ;</span><span class="sxs-lookup"><span data-stu-id="5cd6b-113">HRESULT get\_Chapter(\[out, retval\] long\* plChapter);</span></span>

<span data-ttu-id="5cd6b-114">Placer HRESULT\_chapitre (\[dans\] lChapter long) ;</span><span class="sxs-lookup"><span data-stu-id="5cd6b-114">HRESULT put\_Chapter(\[in\] long lChapter);</span></span>

## <a name="parameters"></a><span data-ttu-id="5cd6b-115">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5cd6b-115">Parameters</span></span>

  - <span data-ttu-id="5cd6b-116">*plChapter*</span><span class="sxs-lookup"><span data-stu-id="5cd6b-116">*plChapter*</span></span>

  - <span data-ttu-id="5cd6b-117">Pointeur vers le descripteur d'un chapitre.</span><span class="sxs-lookup"><span data-stu-id="5cd6b-117">Pointer to the handle of a chapter.</span></span>

  - <span data-ttu-id="5cd6b-118">*LChapter*</span><span class="sxs-lookup"><span data-stu-id="5cd6b-118">*LChapter*</span></span>

  - <span data-ttu-id="5cd6b-119">Descripteur d'un chapitre.</span><span class="sxs-lookup"><span data-stu-id="5cd6b-119">Handle of a chapter.</span></span>

<span data-ttu-id="5cd6b-120"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="5cd6b-120"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="5cd6b-121">Valeurs renvoyées</span><span class="sxs-lookup"><span data-stu-id="5cd6b-121">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="5cd6b-122">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="5cd6b-122">Return values</span></span>
>>>>>>> <span data-ttu-id="5cd6b-123">master</span><span class="sxs-lookup"><span data-stu-id="5cd6b-123">master</span></span>

<span data-ttu-id="5cd6b-124">Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S\_OK et E\_ÉCHOUE.</span><span class="sxs-lookup"><span data-stu-id="5cd6b-124">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="5cd6b-125">Champ d'application</span><span class="sxs-lookup"><span data-stu-id="5cd6b-125">Applies To</span></span>

[<span data-ttu-id="5cd6b-126">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="5cd6b-126">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

