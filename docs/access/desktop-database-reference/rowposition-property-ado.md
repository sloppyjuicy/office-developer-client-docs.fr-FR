---
<span data-ttu-id="34d39-101"><<<<<<< Titre tête : TOCTitle RowPosition propriété (ADO) : RowPosition propriété (ADO) === titre : RowPosition, propriété (ADO) TOCTitle : RowPosition, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="34d39-101"><<<<<<< HEAD title: RowPosition Property (ADO) TOCTitle: RowPosition Property (ADO) ======= title: RowPosition property (ADO) TOCTitle: RowPosition property (ADO)</span></span>
>>>>>>> <span data-ttu-id="34d39-102">Master ms:assetid : b87f14b0-136b-0564-3e12-f9d5ecc4f7c8 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249887(v=office.15) ms:contentKeyID : ms.date 48547325 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="34d39-102">master ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15) ms:contentKeyID: 48547325 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="34d39-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="34d39-103"><<<<<<< HEAD</span></span>
# <a name="rowposition-property-ado"></a><span data-ttu-id="34d39-104">RowPosition, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="34d39-104">RowPosition Property (ADO)</span></span>
=======
# <a name="rowposition-property-ado"></a><span data-ttu-id="34d39-105">RowPosition, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="34d39-105">RowPosition property (ADO)</span></span>
>>>>>>> <span data-ttu-id="34d39-106">master</span><span class="sxs-lookup"><span data-stu-id="34d39-106">master</span></span>


<span data-ttu-id="34d39-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="34d39-107">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="34d39-108">Récupère ou définit un objet **RowPosition** OLE DB à partir de/sur un objet **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="34d39-108">Gets or sets an OLE DB **RowPosition** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="34d39-109">Lorsque vous utilisez **put\_RowPosition** pour définir l’objet **RowPosition** , l’objet **Recordset** résultant utilise l’objet **RowPosition** pour déterminer la ligne active.</span><span class="sxs-lookup"><span data-stu-id="34d39-109">When you use **put\_RowPosition** to set the **RowPosition** object, the resulting **Recordset** object uses the **RowPosition** object to determine the current row.</span></span>

<span data-ttu-id="34d39-110">Lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="34d39-110">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="34d39-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34d39-111">Syntax</span></span>

<span data-ttu-id="34d39-112">Get HRESULT\_RowPosition (\[out, retval\] IUnknown\* \* ppRowPos) ;</span><span class="sxs-lookup"><span data-stu-id="34d39-112">HRESULT get\_RowPosition(\[out, retval\] IUnknown\*\* ppRowPos);</span></span>

<span data-ttu-id="34d39-113">Placer HRESULT\_RowPosition (\[dans\] IUnknown\* pRowPos) ;</span><span class="sxs-lookup"><span data-stu-id="34d39-113">HRESULT put\_RowPosition(\[in\] IUnknown\* pRowPos);</span></span>

## <a name="parameters"></a><span data-ttu-id="34d39-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="34d39-114">Parameters</span></span>

  - <span data-ttu-id="34d39-115">*ppRowPos*</span><span class="sxs-lookup"><span data-stu-id="34d39-115">*ppRowPos*</span></span>

  - <span data-ttu-id="34d39-116">Pointeur vers un objet **RowPosition** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="34d39-116">Pointer to an OLE DB **RowPosition** object.</span></span>

  - <span data-ttu-id="34d39-117">*PRowPos*</span><span class="sxs-lookup"><span data-stu-id="34d39-117">*PRowPos*</span></span>

  - <span data-ttu-id="34d39-118">Objet **RowPosition** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="34d39-118">An OLE DB **RowPosition** object.</span></span>

<span data-ttu-id="34d39-119"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="34d39-119"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="34d39-120">Valeurs renvoyées</span><span class="sxs-lookup"><span data-stu-id="34d39-120">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="34d39-121">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="34d39-121">Return values</span></span>
>>>>>>> <span data-ttu-id="34d39-122">master</span><span class="sxs-lookup"><span data-stu-id="34d39-122">master</span></span>

<span data-ttu-id="34d39-123">Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S\_OK et E\_ÉCHOUE.</span><span class="sxs-lookup"><span data-stu-id="34d39-123">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="34d39-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="34d39-124">Remarks</span></span>

<span data-ttu-id="34d39-125">Lorsque cette propriété est définie, si l’objet **Rowset** de l’objet **RowPosition** est différent de l’objet **Rowset** de l’objet **Recordset** , le premier remplace ce dernier.</span><span class="sxs-lookup"><span data-stu-id="34d39-125">When this property is set, if the **Rowset** object on the **RowPosition** object is different from the **Rowset** object on the **Recordset** object, the former overrides the latter.</span></span> <span data-ttu-id="34d39-126">Le même comportement s’applique au **chapitre** actif à la **RowPosition** .</span><span class="sxs-lookup"><span data-stu-id="34d39-126">The same behavior applies to the current **Chapter** of the **RowPosition** as well.</span></span>

## <a name="applies-to"></a><span data-ttu-id="34d39-127">Champ d'application</span><span class="sxs-lookup"><span data-stu-id="34d39-127">Applies To</span></span>

[<span data-ttu-id="34d39-128">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="34d39-128">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

