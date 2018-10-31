---
<span data-ttu-id="a6595-101"><<<<<<< Titre tête : TOCTitle de la propriété EditMode (ADO) : EditMode propriété (ADO) === titre : EditMode, propriété (ADO) TOCTitle : EditMode, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="a6595-101"><<<<<<< HEAD title: EditMode Property (ADO) TOCTitle: EditMode Property (ADO) ======= title: EditMode property (ADO) TOCTitle: EditMode property (ADO)</span></span>
>>>>>>> <span data-ttu-id="a6595-102">Master ms:assetid : 28ca8f14-abee-ad20-9c16-11bb36b487e4 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249045(v=office.15) ms:contentKeyID : ms.date 48543867 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="a6595-102">master ms:assetid: 28ca8f14-abee-ad20-9c16-11bb36b487e4 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15) ms:contentKeyID: 48543867 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="a6595-103"><<<<<<< EN-TÊTE</span><span class="sxs-lookup"><span data-stu-id="a6595-103"><<<<<<< HEAD</span></span>
# <a name="editmode-property-ado"></a><span data-ttu-id="a6595-104">EditMode, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="a6595-104">EditMode Property (ADO)</span></span>
=======
# <a name="editmode-property-ado"></a><span data-ttu-id="a6595-105">EditMode, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="a6595-105">EditMode property (ADO)</span></span>
>>>>>>> <span data-ttu-id="a6595-106">master</span><span class="sxs-lookup"><span data-stu-id="a6595-106">master</span></span>


<span data-ttu-id="a6595-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a6595-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a6595-108">Indique l'état d'édition de l'enregistrement actuel.</span><span class="sxs-lookup"><span data-stu-id="a6595-108">Indicates the editing status of the current record.</span></span>

<span data-ttu-id="a6595-109"><<<<<<< EN-TÊTE</span><span class="sxs-lookup"><span data-stu-id="a6595-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="a6595-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a6595-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="a6595-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a6595-111">Return value</span></span>
>>>>>>> <span data-ttu-id="a6595-112">master</span><span class="sxs-lookup"><span data-stu-id="a6595-112">master</span></span>

<span data-ttu-id="a6595-113">Renvoie la valeur [EditModeEnum](editmodeenum.md).</span><span class="sxs-lookup"><span data-stu-id="a6595-113">Returns an [EditModeEnum](editmodeenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6595-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a6595-114">Remarks</span></span>

<span data-ttu-id="a6595-p101">ADO gère un tampon d'édition associé à l'enregistrement actuel. Cette propriété indique si des modifications ont été apportées à ce tampon ou si un nouvel enregistrement a été créé. Utilisez la propriété **EditMode** pour déterminer l'état d'édition de l'enregistrement actuel. Vous pouvez tester jusqu'à des modifications si un processus d'édition a été interrompu et détermine si vous devez utiliser la méthode [Update](update-method-ado.md) ou [CancelUpdate](cancelupdate-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a6595-p101">ADO maintains an editing buffer associated with the current record. This property indicates whether changes have been made to this buffer, or whether a new record has been created. Use the **EditMode** property to determine the editing status of the current record. You can test for pending changes if an editing process has been interrupted and determine whether you need to use the [Update](update-method-ado.md) or [CancelUpdate](cancelupdate-method-ado.md) method.</span></span>

<span data-ttu-id="a6595-119">Consultez la méthode [AddNew](addnew-method-ado.md) pour une description plus détaillée de la propriété **EditMode** dans des conditions d'édition différentes.</span><span class="sxs-lookup"><span data-stu-id="a6595-119">See the [AddNew](addnew-method-ado.md) method for a more detailed description of the **EditMode** property under different editing conditions.</span></span>

<span data-ttu-id="a6595-120">Lorsqu’un appel à [Supprimer](delete-method-ado-recordset.md) ne supprime pas correctement l’enregistrement ou des enregistrements dans les données source (en raison de violations d’intégrité référentielle, par exemple), l' [objet Recordset](recordset-object-ado.md) reste en mode édition (**EditMode** = \*\*adEditInProgress \*\*).</span><span class="sxs-lookup"><span data-stu-id="a6595-120">When a call to [Delete](delete-method-ado-recordset.md) does not successfully delete the record or records in the data source (due to referential integrity violations, for example), the [Recordset](recordset-object-ado.md) will remain in edit mode (**EditMode** = **adEditInProgress**).</span></span> <span data-ttu-id="a6595-121">Il faut donc appeler **CancelUpdate** avant de déplacer l'enregistrement actuel (avec [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md) ou [Close](close-method-ado.md), par exemple).</span><span class="sxs-lookup"><span data-stu-id="a6595-121">This means that **CancelUpdate** must be called before moving off the current record (with [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md), or [Close](close-method-ado.md), for example).</span></span>


> [!NOTE]
> <span data-ttu-id="a6595-p103">[!REMARQUE] **EditMode** ne peut renvoyer une valeur valide que s'il existe un enregistrement actuel. **EditMode** renvoie une erreur si la valeur de [BOF or EOF](bof-eof-properties-ado.md) est True ou si l'enregistrement actuel a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="a6595-p103">**EditMode** can return a valid value only if there is a current record. **EditMode** will return an error if [BOF or EOF](bof-eof-properties-ado.md) is true, or if the current record has been deleted.</span></span>


