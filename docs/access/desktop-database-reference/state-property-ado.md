---
<span data-ttu-id="e39fc-101"><<<<<<< Titre tête : TOCTitle état propriété (ADO) : état de propriété (ADO) === titre : State, propriété (ADO) TOCTitle : State, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="e39fc-101"><<<<<<< HEAD title: State Property (ADO) TOCTitle: State Property (ADO) ======= title: State property (ADO) TOCTitle: State property (ADO)</span></span>
>>>>>>> <span data-ttu-id="e39fc-102">Master ms:assetid : ade0a50c-e2d8-23ac-4ea9-b012fedcd5db ms:mtpsurl : https://msdn.microsoft.com/library/JJ249819(v=office.15) ms:contentKeyID : ms.date 48547053 : 18/09/2015 mtps_version : v=office.15 f1_keywords :</span><span class="sxs-lookup"><span data-stu-id="e39fc-102">master ms:assetid: ade0a50c-e2d8-23ac-4ea9-b012fedcd5db ms:mtpsurl: https://msdn.microsoft.com/library/JJ249819(v=office.15) ms:contentKeyID: 48547053 ms.date: 09/18/2015 mtps_version: v=office.15 f1_keywords:</span></span>
- <span data-ttu-id="e39fc-103">Ado210.chm1231176 f1_categories :</span><span class="sxs-lookup"><span data-stu-id="e39fc-103">ado210.chm1231176 f1_categories:</span></span>
- <span data-ttu-id="e39fc-104">Office.Version=v15</span><span class="sxs-lookup"><span data-stu-id="e39fc-104">Office.Version=v15</span></span>
---

<span data-ttu-id="e39fc-105"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="e39fc-105"><<<<<<< HEAD</span></span>
# <a name="state-property-ado"></a><span data-ttu-id="e39fc-106">State, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="e39fc-106">State Property (ADO)</span></span>
=======
# <a name="state-property-ado"></a><span data-ttu-id="e39fc-107">State, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="e39fc-107">State property (ADO)</span></span>
>>>>>>> <span data-ttu-id="e39fc-108">master</span><span class="sxs-lookup"><span data-stu-id="e39fc-108">master</span></span>


<span data-ttu-id="e39fc-109">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e39fc-109">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e39fc-110">Indique, pour tous les objets applicables, si l'état de l'objet est ouvert ou fermé.</span><span class="sxs-lookup"><span data-stu-id="e39fc-110">Indicates for all applicable objects whether the state of the object is open or closed.</span></span>

<span data-ttu-id="e39fc-111">Indique, pour tous les objets applicables exécutant une méthode asynchrone, si l'état actuel de l'objet est « en cours de connexion », « en cours d'exécution » ou « en cours d'extraction ».</span><span class="sxs-lookup"><span data-stu-id="e39fc-111">Indicates for all applicable objects executing an asynchronous method, whether the current state of the object is connecting, executing, or retrieving.</span></span>

<span data-ttu-id="e39fc-112"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="e39fc-112"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="e39fc-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e39fc-113">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="e39fc-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e39fc-114">Return value</span></span>
>>>>>>> <span data-ttu-id="e39fc-115">master</span><span class="sxs-lookup"><span data-stu-id="e39fc-115">master</span></span>

<span data-ttu-id="e39fc-p101">Renvoie une valeur de type **Long** pouvant être une valeur [ObjectStateEnum](objectstateenum.md). La valeur par défaut est **adStateClosed**.</span><span class="sxs-lookup"><span data-stu-id="e39fc-p101">Returns a **Long** value that can be an [ObjectStateEnum](objectstateenum.md) value. The default value is **adStateClosed**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e39fc-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="e39fc-118">Remarks</span></span>

<span data-ttu-id="e39fc-119">Vous pouvez utiliser à tout moment la propriété **State** pour déterminer l'état actuel d'un objet donné.</span><span class="sxs-lookup"><span data-stu-id="e39fc-119">You can use the **State** property to determine the current state of a given object at any time.</span></span>

<span data-ttu-id="e39fc-p102">La propriété **State** de l'objet peut présenter plusieurs valeurs associées. Par exemple, si une instruction est en cours d'exécution, cette propriété aura la valeur **adStateOpen** associée à **adStateExecuting**.</span><span class="sxs-lookup"><span data-stu-id="e39fc-p102">The object's **State** property can have a combination of values. For example, if a statement is executing, this property will have a combined value of **adStateOpen** and **adStateExecuting**.</span></span>

<span data-ttu-id="e39fc-122">La propriété **State** est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e39fc-122">The **State** property is read-only.</span></span>

