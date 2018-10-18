---
<span data-ttu-id="177b7-101"><<<<<<< Titre tête : TOCTitle précision propriété (ADO) : précision propriété (ADO) === titre :, propriété (ADO) de la précision TOCTitle : propriété précision (ADO)</span><span class="sxs-lookup"><span data-stu-id="177b7-101"><<<<<<< HEAD title: Precision Property (ADO) TOCTitle: Precision Property (ADO) ======= title: Precision property (ADO) TOCTitle: Precision property (ADO)</span></span>
>>>>>>> <span data-ttu-id="177b7-102">Master ms:assetid : c9d54d78-d5a5-caf8-d635-259d1fcc0595 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249983(v=office.15) ms:contentKeyID : ms.date 48547685 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="177b7-102">master ms:assetid: c9d54d78-d5a5-caf8-d635-259d1fcc0595 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249983(v=office.15) ms:contentKeyID: 48547685 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="177b7-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="177b7-103"><<<<<<< HEAD</span></span>
# <a name="precision-property-ado"></a><span data-ttu-id="177b7-104">Precision, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="177b7-104">Precision Property (ADO)</span></span>
=======
# <a name="precision-property-ado"></a><span data-ttu-id="177b7-105">Precision, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="177b7-105">Precision property (ADO)</span></span>
>>>>>>> <span data-ttu-id="177b7-106">master</span><span class="sxs-lookup"><span data-stu-id="177b7-106">master</span></span>


<span data-ttu-id="177b7-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="177b7-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="177b7-108">Indique le degré de précision des valeurs numériques d'un objet [Parameter](parameter-object-ado.md) ou d'un objet [Field](field-object-ado.md) numérique.</span><span class="sxs-lookup"><span data-stu-id="177b7-108">Indicates the degree of precision for numeric values in a [Parameter](parameter-object-ado.md) object or for numeric [Field](field-object-ado.md) objects.</span></span>

<span data-ttu-id="177b7-109"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="177b7-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="177b7-110">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="177b7-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="177b7-111">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="177b7-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="177b7-112">master</span><span class="sxs-lookup"><span data-stu-id="177b7-112">master</span></span>

<span data-ttu-id="177b7-113">Définit ou renvoie une valeur de type **Byte** qui indique le nombre maximal de chiffres utilisés pour représenter les valeurs.</span><span class="sxs-lookup"><span data-stu-id="177b7-113">Sets or returns a **Byte** value that indicates the maximum number of digits used to represent values.</span></span>

## <a name="remarks"></a><span data-ttu-id="177b7-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="177b7-114">Remarks</span></span>

<span data-ttu-id="177b7-115">Utilisez la propriété **Précision** pour déterminer le nombre maximal de chiffres utilisés pour représenter les valeurs d'un objet **Parameter** ou **Field** numérique.</span><span class="sxs-lookup"><span data-stu-id="177b7-115">Use the **Precision** property to determine the maximum number of digits used to represent values for a numeric **Parameter** or **Field** object.</span></span>

<span data-ttu-id="177b7-116">Sur un objet **Parameter** cette valeur est accessible lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="177b7-116">The value is read/write on a **Parameter** object.</span></span>

<span data-ttu-id="177b7-p101">Pour un objet **Field**, **Precision** est généralement en lecture seule. Toutefois, pour les objets **Field** récemment ajoutés à la collection [Fields](fields-collection-ado.md) d'un objet [Record](record-object-ado.md), **Precision** est exceptionnellement accessible en lecture et en écriture après la définition de la propriété [Value](value-property-ado.md) de l'objet **Field** et une fois que le fournisseur de données a ajouté le nouvel objet **Field** en appelant la méthode [Update](update-method-ado.md) de la collection **Fields**.</span><span class="sxs-lookup"><span data-stu-id="177b7-p101">For a **Field** object, **Precision** is normally read-only. However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Precision** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

