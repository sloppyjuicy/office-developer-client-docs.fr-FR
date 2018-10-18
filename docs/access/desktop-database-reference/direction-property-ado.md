---
<span data-ttu-id="795b4-101"><<<<<<< Titre tête : TOCTitle Direction propriété (ADO) : Direction propriété (ADO) === titre : Direction, propriété (ADO) TOCTitle : Direction, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="795b4-101"><<<<<<< HEAD title: Direction Property (ADO) TOCTitle: Direction Property (ADO) ======= title: Direction property (ADO) TOCTitle: Direction property (ADO)</span></span>
>>>>>>> <span data-ttu-id="795b4-102">Master ms:assetid : 51a94abb-7ce9-9adb-2b76-5391eb9f6863 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249262(v=office.15) ms:contentKeyID : ms.date 48544823 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="795b4-102">master ms:assetid: 51a94abb-7ce9-9adb-2b76-5391eb9f6863 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249262(v=office.15) ms:contentKeyID: 48544823 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="795b4-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="795b4-103"><<<<<<< HEAD</span></span>
# <a name="direction-property-ado"></a><span data-ttu-id="795b4-104">Direction, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="795b4-104">Direction Property (ADO)</span></span>
=======
# <a name="direction-property-ado"></a><span data-ttu-id="795b4-105">Direction, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="795b4-105">Direction property (ADO)</span></span>
>>>>>>> <span data-ttu-id="795b4-106">master</span><span class="sxs-lookup"><span data-stu-id="795b4-106">master</span></span>


<span data-ttu-id="795b4-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="795b4-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="795b4-108">Indique si l'objet [Parameter](parameter-object-ado.md) représente un paramètre d'entrée, de sortie, d'entrée et de sortie, ou encore si le paramètre est la valeur renvoyée par une procédure stockée.</span><span class="sxs-lookup"><span data-stu-id="795b4-108">Indicates whether the [Parameter](parameter-object-ado.md) represents an input parameter, an output parameter, an input and an output parameter, or if the parameter is the return value from a stored procedure.</span></span>

<span data-ttu-id="795b4-109"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="795b4-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="795b4-110">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="795b4-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="795b4-111">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="795b4-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="795b4-112">master</span><span class="sxs-lookup"><span data-stu-id="795b4-112">master</span></span>

<span data-ttu-id="795b4-113">Définit ou renvoie une valeur [ParameterDirectionEnum](parameterdirectionenum.md).</span><span class="sxs-lookup"><span data-stu-id="795b4-113">Sets or returns a [ParameterDirectionEnum](parameterdirectionenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="795b4-114">Notes</span><span class="sxs-lookup"><span data-stu-id="795b4-114">Remarks</span></span>

<span data-ttu-id="795b4-p101">Utilisez la propriété **Direction** pour spécifier le mode de transmission d'un paramètre dans une procédure. La propriété **Direction** est en lecture-écriture, ce qui vous permet d'utiliser des fournisseurs qui ne retournent pas ces informations ou de définir ces informations lorsque vous ne souhaitez pas qu'ADO effectue un appel supplémentaire au fournisseur pour récupérer des informations de paramètre.</span><span class="sxs-lookup"><span data-stu-id="795b4-p101">Use the **Direction** property to specify how a parameter is passed to or from a procedure. The **Direction** property is read/write; this allows you to work with providers that don't return this information or to set this information when you don't want ADO to make an extra call to the provider to retrieve parameter information.</span></span>

<span data-ttu-id="795b4-p102">Les fournisseurs ne peuvent pas tous déterminer la direction des paramètres dans leurs procédures stockées. En pareil cas, vous devez définir la propriété **Direction** avant d'exécuter la requête.</span><span class="sxs-lookup"><span data-stu-id="795b4-p102">Not all providers can determine the direction of parameters in their stored procedures. In these cases, you must set the **Direction** property before you execute the query.</span></span>

