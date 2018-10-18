---
<span data-ttu-id="4c05e-101"><<<<<<< Titre tête : TOCTitle de la propriété DefinedSize (ADO) : propriété DefinedSize (ADO) === titre : DefinedSize, propriété (ADO) TOCTitle : DefinedSize, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="4c05e-101"><<<<<<< HEAD title: DefinedSize Property (ADO) TOCTitle: DefinedSize Property (ADO) ======= title: DefinedSize property (ADO) TOCTitle: DefinedSize property (ADO)</span></span>
>>>>>>> <span data-ttu-id="4c05e-102">Master ms:assetid : 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249619(v=office.15) ms:contentKeyID : ms.date 48546257 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="4c05e-102">master ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15) ms:contentKeyID: 48546257 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="4c05e-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="4c05e-103"><<<<<<< HEAD</span></span>
# <a name="definedsize-property-ado"></a><span data-ttu-id="4c05e-104">DefinedSize, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="4c05e-104">DefinedSize Property (ADO)</span></span>
=======
# <a name="definedsize-property-ado"></a><span data-ttu-id="4c05e-105">DefinedSize, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="4c05e-105">DefinedSize property (ADO)</span></span>
>>>>>>> <span data-ttu-id="4c05e-106">master</span><span class="sxs-lookup"><span data-stu-id="4c05e-106">master</span></span>


<span data-ttu-id="4c05e-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4c05e-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4c05e-108">Indique la capacité en données d'un objet [Field](field-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4c05e-108">Indicates the data capacity of a [Field](field-object-ado.md) object.</span></span>

<span data-ttu-id="4c05e-109"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="4c05e-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="4c05e-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4c05e-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="4c05e-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4c05e-111">Return value</span></span>
>>>>>>> <span data-ttu-id="4c05e-112">master</span><span class="sxs-lookup"><span data-stu-id="4c05e-112">master</span></span>

<span data-ttu-id="4c05e-113">Renvoie une valeur de type **Long** qui reflète la taille définie pour un champ sous la forme d'un nombre d'octets.</span><span class="sxs-lookup"><span data-stu-id="4c05e-113">Returns a **Long** value that reflects the defined size of a field as a number of bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c05e-114">Notes</span><span class="sxs-lookup"><span data-stu-id="4c05e-114">Remarks</span></span>

<span data-ttu-id="4c05e-115">Utilisez la propriété **DefinedSize** pour déterminer la capacité en données d'un objet **Field**.</span><span class="sxs-lookup"><span data-stu-id="4c05e-115">Use the **DefinedSize** property to determine the data capacity of a **Field** object.</span></span>

<span data-ttu-id="4c05e-p101">Les propriétés **DefinedSize** et [ActualSize](actualsize-property-ado.md) sont différentes. Par exemple, imaginez un objet **Field** avec le type déclaré **adVarChar** et une propriété **DefinedSize** de 50, contenant un caractère unique. La valeur retournée pour la propriété **ActualSize** correspond à la longueur en octets du caractère unique.</span><span class="sxs-lookup"><span data-stu-id="4c05e-p101">The **DefinedSize** and [ActualSize](actualsize-property-ado.md) properties are different. For example, consider a **Field** object with a declared type of **adVarChar** and a **DefinedSize** property value of 50, containing a single character. The **ActualSize** property value it returns is the length in bytes of the single character.</span></span>

