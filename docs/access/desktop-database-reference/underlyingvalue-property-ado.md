---
<span data-ttu-id="fb055-101"><<<<<<< Titre tête : TOCTitle UnderlyingValue propriété (ADO) : propriété UnderlyingValue (ADO) === titre : UnderlyingValue, propriété (ADO) TOCTitle : UnderlyingValue, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="fb055-101"><<<<<<< HEAD title: UnderlyingValue Property (ADO) TOCTitle: UnderlyingValue Property (ADO) ======= title: UnderlyingValue property (ADO) TOCTitle: UnderlyingValue property (ADO)</span></span>
>>>>>>> <span data-ttu-id="fb055-102">Master ms:assetid : f84f4c1c-2bd4-a725-3575-ed063ead13c8 ms:mtpsurl : https://msdn.microsoft.com/library/JJ250262(v=office.15) ms:contentKeyID : ms.date 48548782 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="fb055-102">master ms:assetid: f84f4c1c-2bd4-a725-3575-ed063ead13c8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250262(v=office.15) ms:contentKeyID: 48548782 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="fb055-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="fb055-103"><<<<<<< HEAD</span></span>
# <a name="underlyingvalue-property-ado"></a><span data-ttu-id="fb055-104">UnderlyingValue, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="fb055-104">UnderlyingValue Property (ADO)</span></span>
=======
# <a name="underlyingvalue-property-ado"></a><span data-ttu-id="fb055-105">UnderlyingValue, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="fb055-105">UnderlyingValue property (ADO)</span></span>
>>>>>>> <span data-ttu-id="fb055-106">master</span><span class="sxs-lookup"><span data-stu-id="fb055-106">master</span></span>


<span data-ttu-id="fb055-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fb055-107">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="fb055-108">Indique la valeur actuelle d'un objet [Field](field-object-ado.md) dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="fb055-108">Indicates a [Field](field-object-ado.md) object's current value in the database.</span></span>

<span data-ttu-id="fb055-109"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="fb055-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="fb055-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fb055-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="fb055-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fb055-111">Return value</span></span>
>>>>>>> <span data-ttu-id="fb055-112">master</span><span class="sxs-lookup"><span data-stu-id="fb055-112">master</span></span>

<span data-ttu-id="fb055-113">Renvoie une valeur **Variant** qui indique la valeur de l'objet **Field**.</span><span class="sxs-lookup"><span data-stu-id="fb055-113">Returns a **Variant** value that indicates the value of the **Field**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb055-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="fb055-114">Remarks</span></span>

<span data-ttu-id="fb055-p101">Utilisez la propriété **UnderlyingValue** pour renvoyer la valeur actuelle du champ de la base de données. La valeur du champ dans la propriété **UnderlyingValue** est celle qui est visible pour votre transaction et peut résulter d'une mise à jour récente effectuée par une autre transaction. Elle peut être différente de la propriété [OriginalValue](originalvalue-property-ado.md), qui reflète la valeur renvoyée à l'origine à l'objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="fb055-p101">Use the **UnderlyingValue** property to return the current field value from the database. The field value in the **UnderlyingValue** property is the value that is visible to your transaction and may be the result of a recent update by another transaction. This may differ from the [OriginalValue](originalvalue-property-ado.md) property, which reflects the value that was originally returned to the [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="fb055-p102">Cette procédure est similaire à la méthode [Resync](resync-method-ado.md), mais la propriété **UnderlyingValue** renvoie uniquement la valeur d'un champ spécifique de l'enregistrement actuel. C'est cette valeur que la méthode [Resync](resync-method-ado.md) utilise pour remplacer la propriété [Value](value-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="fb055-p102">This is similar to using the [Resync](resync-method-ado.md) method, but the **UnderlyingValue** property returns only the value for a specific field from the current record. This is the same value that the [Resync](resync-method-ado.md) method uses to replace the [Value](value-property-ado.md) property.</span></span>

<span data-ttu-id="fb055-120">Lorsque vous utilisez cette propriété en association avec la propriété **OriginalValue**, vous pouvez résoudre les conflits générés par les mises à jour par lot.</span><span class="sxs-lookup"><span data-stu-id="fb055-120">When you use this property with the **OriginalValue** property, you can resolve conflicts that arise from batch updates.</span></span>

## <a name="record"></a><span data-ttu-id="fb055-121">Rappel</span><span class="sxs-lookup"><span data-stu-id="fb055-121">Record</span></span>

<span data-ttu-id="fb055-122">Pour les objets [Record](record-object-ado.md), cette propriété est vide pour les champs ajoutés avant l'appel de la méthode [Update](update-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="fb055-122">For [Record](record-object-ado.md) objects, this property will be empty for fields added before [Update](update-method-ado.md) is called.</span></span>

