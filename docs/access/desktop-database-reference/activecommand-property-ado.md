---
<span data-ttu-id="eeac0-101"><<<<<<< Titre tête : TOCTitle ActiveCommand propriété (ADO) : ms:assetid ActiveCommand propriété (ADO) : 41c19008-cbf7-ade9-b4ab-e908a16784ac ms:mtpsurl : https://msdn.microsoft.com/library/JJ249190(v=office.15) ms:contentKeyID : ms.date 48544459 : mtps_version 18/09/2015 : v = Office.15</span><span class="sxs-lookup"><span data-stu-id="eeac0-101"><<<<<<< HEAD title: ActiveCommand Property (ADO) TOCTitle: ActiveCommand Property (ADO) ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15) ms:contentKeyID: 48544459 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

# <a name="activecommand-property-ado"></a><span data-ttu-id="eeac0-102">ActiveCommand, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="eeac0-102">ActiveCommand Property (ADO)</span></span>

<span data-ttu-id="eeac0-103">=== titre : ActiveCommand, propriété (ADO) TOCTitle : ActiveCommand, propriété (ADO) ms:assetid : 41c19008-cbf7-ade9-b4ab-e908a16784ac ms:mtpsurl : https://msdn.microsoft.com/library/JJ249190(v=office.15) ms:contentKeyID : ms.date 48544459 : 17/10/2018 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="eeac0-103">======= title: ActiveCommand property (ADO) TOCTitle: ActiveCommand property (ADO) ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15) ms:contentKeyID: 48544459 ms.date: 10/17/2018 mtps_version: v=office.15</span></span>
---

# <a name="activecommand-property-ado"></a><span data-ttu-id="eeac0-104">ActiveCommand, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="eeac0-104">ActiveCommand property (ADO)</span></span>
>>>>>>> <span data-ttu-id="eeac0-105">master</span><span class="sxs-lookup"><span data-stu-id="eeac0-105">master</span></span>

<span data-ttu-id="eeac0-106">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="eeac0-106">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="eeac0-107">Indique l'objet [Command](command-object-ado.md) qui a créé l'objet [Recordset](recordset-object-ado.md) associé.</span><span class="sxs-lookup"><span data-stu-id="eeac0-107">Indicates the [Command](command-object-ado.md) object that created the associated [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="eeac0-108"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="eeac0-108"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="eeac0-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="eeac0-109">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="eeac0-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="eeac0-110">Return value</span></span>
>>>>>>> <span data-ttu-id="eeac0-111">master</span><span class="sxs-lookup"><span data-stu-id="eeac0-111">master</span></span>

<span data-ttu-id="eeac0-p101">Renvoie une valeur de type **Variant** qui contient un objet **Command**. La valeur par défaut est une référence d'objet Null.</span><span class="sxs-lookup"><span data-stu-id="eeac0-p101">Returns a **Variant** that contains a **Command** object. Default is a null object reference.</span></span>

## <a name="remarks"></a><span data-ttu-id="eeac0-114">Notes</span><span class="sxs-lookup"><span data-stu-id="eeac0-114">Remarks</span></span>

<span data-ttu-id="eeac0-115">La propriété **ActiveCommand** est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="eeac0-115">The **ActiveCommand** property is read-only.</span></span>

<span data-ttu-id="eeac0-116"><<<<<<< Tête si un objet **Command** n’a pas été utilisé pour créer l' **objet Recordset**actif, puis une référence d’objet **Null** est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="eeac0-116"><<<<<<< HEAD If a **Command** object was not used to create the current **Recordset**, then a **Null** object reference is returned.</span></span>
<span data-ttu-id="eeac0-117">=== Si un objet **Command** n’était pas utilisé pour créer l' **objet Recordset**actif, une référence d’objet **Null** est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="eeac0-117">======= If a **Command** object was not used to create the current **Recordset**, a **Null** object reference is returned.</span></span>
>>>>>>> <span data-ttu-id="eeac0-118">master</span><span class="sxs-lookup"><span data-stu-id="eeac0-118">master</span></span>

<span data-ttu-id="eeac0-119">Utilisez cette propriété pour rechercher l'objet **Command** associé lorsque vous ne recevez que l'objet **Recordset** qui en résulte.</span><span class="sxs-lookup"><span data-stu-id="eeac0-119">Use this property to find the associated **Command** object when you are given only the resulting **Recordset** object.</span></span>

