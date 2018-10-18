---
<span data-ttu-id="8ffa4-101"><<<<<<< Titre tête : TOCTitle Type propriété (ADO) : Type de propriété (ADO) === titre : Type, propriété (ADO) TOCTitle : Type, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="8ffa4-101"><<<<<<< HEAD title: Type Property (ADO) TOCTitle: Type Property (ADO) ======= title: Type property (ADO) TOCTitle: Type property (ADO)</span></span>
>>>>>>> <span data-ttu-id="8ffa4-102">Master ms:assetid : 14d99172-2145-05ae-620b-459ba097f05c ms:mtpsurl : https://msdn.microsoft.com/library/JJ248914(v=office.15) ms:contentKeyID : ms.date 48543397 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="8ffa4-102">master ms:assetid: 14d99172-2145-05ae-620b-459ba097f05c ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15) ms:contentKeyID: 48543397 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="8ffa4-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="8ffa4-103"><<<<<<< HEAD</span></span>
# <a name="type-property-ado"></a><span data-ttu-id="8ffa4-104">Type, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="8ffa4-104">Type Property (ADO)</span></span>
=======
# <a name="type-property-ado"></a><span data-ttu-id="8ffa4-105">Type, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="8ffa4-105">Type property (ADO)</span></span>
>>>>>>> <span data-ttu-id="8ffa4-106">master</span><span class="sxs-lookup"><span data-stu-id="8ffa4-106">master</span></span>


<span data-ttu-id="8ffa4-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8ffa4-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8ffa4-108">Indique le type opérationnel ou le type de données de l'objet [Parameter](parameter-object-ado.md), [Field](field-object-ado.md) ou [Property](property-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="8ffa4-108">Indicates the operational type or data type of a [Parameter](parameter-object-ado.md), [Field](field-object-ado.md), or [Property](property-object-ado.md) object.</span></span>

<span data-ttu-id="8ffa4-109"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="8ffa4-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="8ffa4-110">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="8ffa4-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="8ffa4-111">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="8ffa4-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="8ffa4-112">master</span><span class="sxs-lookup"><span data-stu-id="8ffa4-112">master</span></span>

<span data-ttu-id="8ffa4-113">Définit ou renvoie une valeur [DataTypeEnum](datatypeenum.md).</span><span class="sxs-lookup"><span data-stu-id="8ffa4-113">Sets or returns a [DataTypeEnum](datatypeenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ffa4-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="8ffa4-114">Remarks</span></span>

<span data-ttu-id="8ffa4-p101">La propriété **Type** est en lecture/écriture pour les objets **Parameter**. Pour les nouveaux objets **Field** ayant été ajoutés à la collection [Fields](fields-collection-ado.md) d'un objet [Record](record-object-ado.md), la propriété **Type** n'est accessible en lecture et en écriture qu'une fois que la propriété [Value](value-property-ado.md) de l'objet **Field** est spécifiée et que le fournisseur de données a correctement ajouté le nouvel objet **Field** en appelant la méthode [Update](update-method-ado.md) de la collection **Fields**.</span><span class="sxs-lookup"><span data-stu-id="8ffa4-p101">For **Parameter** objects, the **Type** property is read/write. For new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Type** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="8ffa4-117">Pour tous les autres objets, la propriété **Type** est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="8ffa4-117">For all other objects, the **Type** property is read-only.</span></span>

