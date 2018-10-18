---
<span data-ttu-id="4c6a7-101"><<<<<<< Titre tête : TOCTitle StayInSync propriété (ADO) : propriété StayInSync (ADO) === titre : StayInSync, propriété (ADO) TOCTitle : StayInSync, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="4c6a7-101"><<<<<<< HEAD title: StayInSync Property (ADO) TOCTitle: StayInSync Property (ADO) ======= title: StayInSync property (ADO) TOCTitle: StayInSync property (ADO)</span></span>
>>>>>>> <span data-ttu-id="4c6a7-102">Master ms:assetid : 02c95c10-4032-14e1-e506-f334a8787142 ms:mtpsurl : https://msdn.microsoft.com/library/JJ248792(v=office.15) ms:contentKeyID : ms.date 48542966 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="4c6a7-102">master ms:assetid: 02c95c10-4032-14e1-e506-f334a8787142 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248792(v=office.15) ms:contentKeyID: 48542966 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="4c6a7-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="4c6a7-103"><<<<<<< HEAD</span></span>
# <a name="stayinsync-property-ado"></a><span data-ttu-id="4c6a7-104">StayInSync, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="4c6a7-104">StayInSync Property (ADO)</span></span>
=======
# <a name="stayinsync-property-ado"></a><span data-ttu-id="4c6a7-105">StayInSync, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="4c6a7-105">StayInSync property (ADO)</span></span>
>>>>>>> <span data-ttu-id="4c6a7-106">master</span><span class="sxs-lookup"><span data-stu-id="4c6a7-106">master</span></span>


<span data-ttu-id="4c6a7-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4c6a7-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4c6a7-108">Indique, dans un objet [Recordset](recordset-object-ado.md) hiérarchique, si la référence aux enregistrements enfants sous-jacents (c'est-à-dire, le *chapitre*) change en même temps que la position de la ligne parente.</span><span class="sxs-lookup"><span data-stu-id="4c6a7-108">Indicates, in a hierarchical [Recordset](recordset-object-ado.md) object, whether the reference to the underlying child records (that is, the *chapter*) changes when the parent row position changes.</span></span>

<span data-ttu-id="4c6a7-109"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="4c6a7-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="4c6a7-110">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="4c6a7-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="4c6a7-111">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="4c6a7-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="4c6a7-112">master</span><span class="sxs-lookup"><span data-stu-id="4c6a7-112">master</span></span>

<span data-ttu-id="4c6a7-p101">Définit ou renvoie une valeur de type **Boolean**. La valeur par défaut est **True**. Avec une valeur **True**, le chapitre est mis à jour lorsque l'objet **Recordset** parent change de position de ligne ; en cas de valeur **False**, le chapitre continue à faire référence aux données du chapitre précédent même si l'objet **Recordset** parent a changé de position de ligne.</span><span class="sxs-lookup"><span data-stu-id="4c6a7-p101">Sets or returns a **Boolean** value. The default value is **True**. If **True**, the chapter will be updated if the parent **Recordset** object changes row position; if **False**, the chapter will continue to refer to data in the previous chapter even though the parent **Recordset** object has changed row position.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c6a7-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="4c6a7-116">Remarks</span></span>

<span data-ttu-id="4c6a7-p102">Cette propriété s'applique aux objets Recordset hiérarchiques, comme ceux pris en charge par [Microsoft Data Shaping Service pour OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) et doit être définie sur le **Recordset** parent avant que le **Recordset** ne soit extrait. Cette propriété simplifie la navigation dans les jeux d'enregistrements hiérarchiques.</span><span class="sxs-lookup"><span data-stu-id="4c6a7-p102">This property applies to hierarchical Recordsets, such as those supported by the [Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), and must be set on the parent **Recordset** before the child **Recordset** is retrieved. This property simplifies navigating hierarchical recordsets.</span></span>

