---
<span data-ttu-id="5242b-101"><<<<<<< Titre tête : TOCTitle de la propriété OriginalValue (ADO) : propriété OriginalValue (ADO) === titre : OriginalValue, propriété (ADO) TOCTitle : OriginalValue, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="5242b-101"><<<<<<< HEAD title: OriginalValue Property (ADO) TOCTitle: OriginalValue Property (ADO) ======= title: OriginalValue property (ADO) TOCTitle: OriginalValue property (ADO)</span></span>
>>>>>>> <span data-ttu-id="5242b-102">Master ms:assetid : 02ffc728-4692-d439-e2a6-2f02cca53a71 ms:mtpsurl : https://msdn.microsoft.com/library/JJ248798(v=office.15) ms:contentKeyID : ms.date 48542974 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="5242b-102">master ms:assetid: 02ffc728-4692-d439-e2a6-2f02cca53a71 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248798(v=office.15) ms:contentKeyID: 48542974 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="5242b-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="5242b-103"><<<<<<< HEAD</span></span>
# <a name="originalvalue-property-ado"></a><span data-ttu-id="5242b-104">OriginalValue, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="5242b-104">OriginalValue Property (ADO)</span></span>
=======
# <a name="originalvalue-property-ado"></a><span data-ttu-id="5242b-105">OriginalValue, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="5242b-105">OriginalValue property (ADO)</span></span>
>>>>>>> <span data-ttu-id="5242b-106">master</span><span class="sxs-lookup"><span data-stu-id="5242b-106">master</span></span>

<span data-ttu-id="5242b-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5242b-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5242b-108">Indique la valeur d'un objet [Field](field-object-ado.md) existant dans l'enregistrement avant qu'aucune modification n'ait été apportée.</span><span class="sxs-lookup"><span data-stu-id="5242b-108">Indicates the value of a [Field](field-object-ado.md) that existed in the record before any changes were made.</span></span>

<span data-ttu-id="5242b-109"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="5242b-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="5242b-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5242b-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="5242b-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5242b-111">Return value</span></span>
>>>>>>> <span data-ttu-id="5242b-112">master</span><span class="sxs-lookup"><span data-stu-id="5242b-112">master</span></span>

<span data-ttu-id="5242b-113">Renvoie une valeur **Variant** représentant la valeur d'un champ avant modification.</span><span class="sxs-lookup"><span data-stu-id="5242b-113">Returns a **Variant** value that represents the value of a field prior to any change.</span></span>

## <a name="remarks"></a><span data-ttu-id="5242b-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="5242b-114">Remarks</span></span>

<span data-ttu-id="5242b-115">Utilisez la propriété **OriginalValue** pour renvoyer la valeur d'origine d'un champ depuis l'enregistrement actuel.</span><span class="sxs-lookup"><span data-stu-id="5242b-115">Use the **OriginalValue** property to return the original field value for a field from the current record.</span></span>

<span data-ttu-id="5242b-116">En *mode de mise à jour immédiate* (dans lequel le fournisseur écrit les modifications dans la source de données sous-jacente après l’appel de la méthode [Update](update-method-ado.md) ), la propriété **OriginalValue** renvoie la valeur du champ qui existait avant toute modification (c'est-à-dire, dans la mesure où le le dernier appel de la méthode **mise à jour** ).</span><span class="sxs-lookup"><span data-stu-id="5242b-116">In *immediate update mode* (in which the provider writes changes to the underlying data source after you call the [Update](update-method-ado.md) method), the **OriginalValue** property returns the field value that existed prior to any changes (that is, since the last **Update** method call).</span></span> <span data-ttu-id="5242b-117">C'est la même valeur que la méthode [CancelUpdate](cancelupdate-method-ado.md) utilise pour remplacer la propriété [Value](value-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="5242b-117">This is the same value that the [CancelUpdate](cancelupdate-method-ado.md) method uses to replace the [Value](value-property-ado.md) property.</span></span>

<span data-ttu-id="5242b-118">En *mode de mise à jour par lot* (dans lequel le fournisseur met en cache plusieurs modifications et les écrit dans la source de données sous-jacente uniquement lorsque vous appelez la méthode [UpdateBatch](updatebatch-method-ado.md) ), la propriété **OriginalValue** renvoie la valeur du champ qui existait avant les change (autrement dit, dans la mesure où la méthode **UpdateBatch** dernier appel).</span><span class="sxs-lookup"><span data-stu-id="5242b-118">In *batch update mode* (in which the provider caches multiple changes and writes them to the underlying data source only when you call the [UpdateBatch](updatebatch-method-ado.md) method), the **OriginalValue** property returns the field value that existed prior to any changes (that is, since the last **UpdateBatch** method call).</span></span> <span data-ttu-id="5242b-119">C'est cette valeur que la méthode [CancelBatch](cancelbatch-method-ado.md) utilise pour remplacer la propriété **Value**.</span><span class="sxs-lookup"><span data-stu-id="5242b-119">This is the same value that the [CancelBatch](cancelbatch-method-ado.md) method uses to replace the **Value** property.</span></span> <span data-ttu-id="5242b-120">Lorsque vous utilisez cette propriété en association avec la propriété [UnderlyingValue](underlyingvalue-property-ado.md), vous pouvez résoudre les conflits générés par les mises à jour par lot.</span><span class="sxs-lookup"><span data-stu-id="5242b-120">When you use this property with the [UnderlyingValue](underlyingvalue-property-ado.md) property, you can resolve conflicts that arise from batch updates.</span></span>

## <a name="record"></a><span data-ttu-id="5242b-121">Rappel</span><span class="sxs-lookup"><span data-stu-id="5242b-121">Record</span></span>

<span data-ttu-id="5242b-122">Pour les objets [Record](record-object-ado.md), la propriété **OriginalValue** est vide pour les champs ajoutés avant l'appel de la méthode [Update](update-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="5242b-122">For [Record](record-object-ado.md) objects, the **OriginalValue** property will be empty for fields added before [Update](update-method-ado.md) is called.</span></span>

