---
<span data-ttu-id="6a037-101"><<<<<<< Titre tête : TOCTitle Description propriété (ADO) : Description propriété (ADO) === titre : Description, propriété (ADO) TOCTitle : Description, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="6a037-101"><<<<<<< HEAD title: Description Property (ADO) TOCTitle: Description Property (ADO) ======= title: Description property (ADO) TOCTitle: Description property (ADO)</span></span>
>>>>>>> <span data-ttu-id="6a037-102">Master ms:assetid : 31df5e36-641c-d213-31fc-6244e2983327 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249092(v=office.15) ms:contentKeyID : ms.date 48544064 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="6a037-102">master ms:assetid: 31df5e36-641c-d213-31fc-6244e2983327 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15) ms:contentKeyID: 48544064 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="6a037-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="6a037-103"><<<<<<< HEAD</span></span>
# <a name="description-property-ado"></a><span data-ttu-id="6a037-104">Description, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="6a037-104">Description Property (ADO)</span></span>
=======
# <a name="description-property-ado"></a><span data-ttu-id="6a037-105">Description, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="6a037-105">Description property (ADO)</span></span>
>>>>>>> <span data-ttu-id="6a037-106">master</span><span class="sxs-lookup"><span data-stu-id="6a037-106">master</span></span>


<span data-ttu-id="6a037-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6a037-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6a037-108">Décrit un objet [Error](error-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="6a037-108">Describes an [Error](error-object-ado.md) object.</span></span>

<span data-ttu-id="6a037-109"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="6a037-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="6a037-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6a037-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="6a037-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6a037-111">Return value</span></span>
>>>>>>> <span data-ttu-id="6a037-112">master</span><span class="sxs-lookup"><span data-stu-id="6a037-112">master</span></span>

<span data-ttu-id="6a037-113">Renvoie une valeur de type **String** qui contient une description de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="6a037-113">Returns a **String** value that contains a description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a037-114">Notes</span><span class="sxs-lookup"><span data-stu-id="6a037-114">Remarks</span></span>

<span data-ttu-id="6a037-p101">Utilisez la propriété **Description** pour obtenir une courte description de l'erreur. Affichez cette propriété pour avertir l'utilisateur d'une erreur que vous ne pouvez pas ou ne souhaitez pas gérer. La chaîne provient d'ADO ou d'un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="6a037-p101">Use the **Description** property to obtain a short description of the error. Display this property to alert the user to an error that you cannot or do not want to handle. The string will come from either ADO or a provider.</span></span>

<span data-ttu-id="6a037-p102">Les fournisseurs sont chargés de transmettre un texte d'erreur spécifique à ADO. ADO ajoute un objet [Error](error-object-ado.md) à la collection **Errors** pour chaque erreur ou avertissement de fournisseur reçu. Énumérez la collection **Errors** pour identifier les erreurs transmises par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="6a037-p102">Providers are responsible for passing specific error text to ADO. ADO adds an [Error](error-object-ado.md) object to the **Errors** collection for each provider error or warning it receives. Enumerate the **Errors** collection to trace the errors that the provider passes.</span></span>

