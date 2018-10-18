---
<span data-ttu-id="f2867-101">titre : Row, propriété - ActiveX Data Objects (ADO) <<<<<<< TOCTitle tête : ligne de propriété (ADO) === TOCTitle : Row, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="f2867-101">title: Row Property - ActiveX Data Objects (ADO) <<<<<<< HEAD TOCTitle: Row Property (ADO) ======= TOCTitle: Row property (ADO)</span></span>
>>>>>>> <span data-ttu-id="f2867-102">Master ms:assetid : 1c2b0e27-7232-4b1c-826c-9dc15d758851 ms:mtpsurl : https://msdn.microsoft.com/library/JJ248959(v=office.15) ms:contentKeyID : ms.date 48543562 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="f2867-102">master ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15) ms:contentKeyID: 48543562 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="f2867-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="f2867-103"><<<<<<< HEAD</span></span>
# <a name="row-property-ado"></a><span data-ttu-id="f2867-104">Row, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="f2867-104">Row Property (ADO)</span></span>
=======
# <a name="row-property-ado"></a><span data-ttu-id="f2867-105">Row, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="f2867-105">Row property (ADO)</span></span>
>>>>>>> <span data-ttu-id="f2867-106">master</span><span class="sxs-lookup"><span data-stu-id="f2867-106">master</span></span>


<span data-ttu-id="f2867-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f2867-107">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="f2867-108">Extrait ou définit un objet **Row** OLE DB à partir de ou sur un objet **ADORecordConstruction**.</span><span class="sxs-lookup"><span data-stu-id="f2867-108">Gets or sets an OLE DB **Row** object from/on an **ADORecordConstruction** object.</span></span> <span data-ttu-id="f2867-109">Lorsque vous utilisez **put\_ligne** pour définir un objet **Row** , une ligne est transformée en objet ADO **Record** .</span><span class="sxs-lookup"><span data-stu-id="f2867-109">When you use **put\_Row** to set a **Row** object, a row is turned into an ADO **Record** object.</span></span> <span data-ttu-id="f2867-110">Lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="f2867-110">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2867-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2867-111">Syntax</span></span>

<span data-ttu-id="f2867-112">Get HRESULT\_ligne (\[out, retval\] IUnknown\* \* ppRow) ;</span><span class="sxs-lookup"><span data-stu-id="f2867-112">HRESULT get\_Row(\[out, retval\] IUnknown\*\* ppRow);</span></span>

<span data-ttu-id="f2867-113">Placer HRESULT\_ligne (\[dans\] IUnknown\* pRow) ;</span><span class="sxs-lookup"><span data-stu-id="f2867-113">HRESULT put\_Row(\[in\] IUnknown\* pRow);</span></span>

## <a name="parameters"></a><span data-ttu-id="f2867-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2867-114">Parameters</span></span>

  - <span data-ttu-id="f2867-115">*ppRow*</span><span class="sxs-lookup"><span data-stu-id="f2867-115">*ppRow*</span></span>

  - <span data-ttu-id="f2867-116">Pointeur vers un objet **Row** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="f2867-116">Pointer to an OLE DB **Row** object.</span></span>

  - <span data-ttu-id="f2867-117">*PRow*</span><span class="sxs-lookup"><span data-stu-id="f2867-117">*PRow*</span></span>

  - <span data-ttu-id="f2867-118">Objet **Row** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="f2867-118">An OLE DB **Row** object.</span></span>

<span data-ttu-id="f2867-119"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="f2867-119"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="f2867-120">Valeurs renvoyées</span><span class="sxs-lookup"><span data-stu-id="f2867-120">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="f2867-121">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="f2867-121">Return values</span></span>
>>>>>>> <span data-ttu-id="f2867-122">master</span><span class="sxs-lookup"><span data-stu-id="f2867-122">master</span></span>

<span data-ttu-id="f2867-123">Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S\_OK et E\_ÉCHOUE.</span><span class="sxs-lookup"><span data-stu-id="f2867-123">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="f2867-124">Champ d'application</span><span class="sxs-lookup"><span data-stu-id="f2867-124">Applies To</span></span>

[<span data-ttu-id="f2867-125">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="f2867-125">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

