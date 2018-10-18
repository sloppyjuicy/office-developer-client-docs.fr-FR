---
<span data-ttu-id="5d8b6-101"><<<<<<< Titre tête : TOCTitle fournisseur propriété (ADO) : fournisseur de propriété (ADO) === titre : propriété Provider (ADO) TOCTitle : propriété Provider (ADO)</span><span class="sxs-lookup"><span data-stu-id="5d8b6-101"><<<<<<< HEAD title: Provider Property (ADO) TOCTitle: Provider Property (ADO) ======= title: Provider property (ADO) TOCTitle: Provider property (ADO)</span></span>
>>>>>>> <span data-ttu-id="5d8b6-102">Master ms:assetid : 1b795f51-93d7-431c-b1fe-0db95f69a56a ms:mtpsurl : https://msdn.microsoft.com/library/JJ248953(v=office.15) ms:contentKeyID : ms.date 48543543 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="5d8b6-102">master ms:assetid: 1b795f51-93d7-431c-b1fe-0db95f69a56a ms:mtpsurl: https://msdn.microsoft.com/library/JJ248953(v=office.15) ms:contentKeyID: 48543543 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="5d8b6-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="5d8b6-103"><<<<<<< HEAD</span></span>
# <a name="provider-property-ado"></a><span data-ttu-id="5d8b6-104">Provider, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="5d8b6-104">Provider Property (ADO)</span></span>
=======
# <a name="provider-property-ado"></a><span data-ttu-id="5d8b6-105">Propriété Provider (ADO)</span><span class="sxs-lookup"><span data-stu-id="5d8b6-105">Provider property (ADO)</span></span>
>>>>>>> <span data-ttu-id="5d8b6-106">master</span><span class="sxs-lookup"><span data-stu-id="5d8b6-106">master</span></span>


<span data-ttu-id="5d8b6-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5d8b6-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5d8b6-108">Indique le nom du fournisseur d'un objet [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="5d8b6-108">Indicates the name of the provider for a [Connection](connection-object-ado.md) object.</span></span>

<span data-ttu-id="5d8b6-109"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="5d8b6-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="5d8b6-110">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="5d8b6-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="5d8b6-111">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="5d8b6-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="5d8b6-112">master</span><span class="sxs-lookup"><span data-stu-id="5d8b6-112">master</span></span>

<span data-ttu-id="5d8b6-113">Définit ou renvoie une valeur **String** qui indique le nom du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="5d8b6-113">Sets or returns a **String** value that indicates the provider name.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d8b6-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="5d8b6-114">Remarks</span></span>

<span data-ttu-id="5d8b6-p101">Utilisez la propriété **Provider** pour définir ou renvoyer le nom du fournisseur d’une connexion. Cette propriété peut aussi être définie par le contenu de la propriété [ConnectionString](connectionstring-property-ado.md) ou de l’argument *ConnectionString* de la méthode [Open](open-method-ado-connection.md). Toutefois, si l’on indique le fournisseur à plusieurs endroits et que l’on appelle la méthode **Open**, les résultats sont imprévisibles. Si aucun fournisseur n’est spécifié, la valeur par défaut de la propriété est MSDASQL ([Fournisseur Microsoft OLE DB pour ODBC](microsoft-ole-db-provider-for-odbc.md)).</span><span class="sxs-lookup"><span data-stu-id="5d8b6-p101">Use the **Provider** property to set or return the name of the provider for a connection. This property can also be set by the contents of the [ConnectionString](connectionstring-property-ado.md) property or the *ConnectionString* argument of the [Open](open-method-ado-connection.md) method; however, specifying a provider in more than one place while calling the **Open** method can have unpredictable results. If no provider is specified, the property will default to MSDASQL ([Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md)).</span></span>

<span data-ttu-id="5d8b6-p102">La propriété **Provider** est en lecture/écriture lorsque la connexion est fermée et en lecture seule lorsqu'elle est ouverte. Le paramètre ne prend que lorsque l'on ouvre l'objet **Connection** ou que l'on accède à la collection [Properties](properties-collection-ado.md) de l'objet **Connection**. Si le paramètre n'est pas valide, une erreur est générée.</span><span class="sxs-lookup"><span data-stu-id="5d8b6-p102">The **Provider** property is read/write when the connection is closed and read-only when it is open. The setting does not take effect until you either open the **Connection** object or access the [Properties](properties-collection-ado.md) collection of the **Connection** object. If the setting is not valid, an error occurs.</span></span>

