---
<span data-ttu-id="05e4f-101"><<<<<<< Titre tête : TOCTitle Rowset propriété (ADO) : Rowset propriété (ADO) === titre : Rowset, propriété (ADO) TOCTitle : Rowset, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="05e4f-101"><<<<<<< HEAD title: Rowset Property (ADO) TOCTitle: Rowset Property (ADO) ======= title: Rowset property (ADO) TOCTitle: Rowset property (ADO)</span></span>
>>>>>>> <span data-ttu-id="05e4f-102">Master ms:assetid : 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53 ms:mtpsurl : https://msdn.microsoft.com/library/JJ248946(v=office.15) ms:contentKeyID : ms.date 48543515 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="05e4f-102">master ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15) ms:contentKeyID: 48543515 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="05e4f-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="05e4f-103"><<<<<<< HEAD</span></span>
# <a name="rowset-property-ado"></a><span data-ttu-id="05e4f-104">Rowset, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="05e4f-104">Rowset Property (ADO)</span></span>
=======
# <a name="rowset-property-ado"></a><span data-ttu-id="05e4f-105">Rowset, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="05e4f-105">Rowset property (ADO)</span></span>
>>>>>>> <span data-ttu-id="05e4f-106">master</span><span class="sxs-lookup"><span data-stu-id="05e4f-106">master</span></span>


<span data-ttu-id="05e4f-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="05e4f-107">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="05e4f-108">Récupère ou définit un objet **Rowset** OLE DB sur un objet **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="05e4f-108">Gets or sets an OLE DB **Rowset** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="05e4f-109">Lorsque vous utilisez put\_Rowset, l’ensemble de lignes est transformé en un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="05e4f-109">When you use put\_Rowset, the rowset is turned into an ADO **Recordset** object.</span></span>

<span data-ttu-id="05e4f-110">Lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="05e4f-110">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="05e4f-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05e4f-111">Syntax</span></span>

<span data-ttu-id="05e4f-112">Get HRESULT\_Rowset (\[out, retval\] IUnknown\* \* ppRowset) ;</span><span class="sxs-lookup"><span data-stu-id="05e4f-112">HRESULT get\_Rowset(\[out, retval\] IUnknown\*\* ppRowset);</span></span>

<span data-ttu-id="05e4f-113">Placer HRESULT\_Rowset (\[dans\] IUnknown\* pRowset) ;</span><span class="sxs-lookup"><span data-stu-id="05e4f-113">HRESULT put\_Rowset(\[in\] IUnknown\* pRowset);</span></span>

## <a name="parameters"></a><span data-ttu-id="05e4f-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05e4f-114">Parameters</span></span>

  - <span data-ttu-id="05e4f-115">*ppRowset*</span><span class="sxs-lookup"><span data-stu-id="05e4f-115">*ppRowset*</span></span>

  - <span data-ttu-id="05e4f-116">Pointeur vers un objet **Rowset** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="05e4f-116">Pointer to an OLE DB **Rowset** object.</span></span>

  - <span data-ttu-id="05e4f-117">*PRowset*</span><span class="sxs-lookup"><span data-stu-id="05e4f-117">*PRowset*</span></span>

  - <span data-ttu-id="05e4f-118">Objet **Rowset** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="05e4f-118">An OLE DB **Rowset** object.</span></span>

<span data-ttu-id="05e4f-119"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="05e4f-119"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="05e4f-120">Valeurs renvoyées</span><span class="sxs-lookup"><span data-stu-id="05e4f-120">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="05e4f-121">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="05e4f-121">Return values</span></span>
>>>>>>> <span data-ttu-id="05e4f-122">master</span><span class="sxs-lookup"><span data-stu-id="05e4f-122">master</span></span>

<span data-ttu-id="05e4f-123">Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S\_OK et E\_ÉCHOUE.</span><span class="sxs-lookup"><span data-stu-id="05e4f-123">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="05e4f-124">Champ d'application</span><span class="sxs-lookup"><span data-stu-id="05e4f-124">Applies To</span></span>

[<span data-ttu-id="05e4f-125">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="05e4f-125">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

