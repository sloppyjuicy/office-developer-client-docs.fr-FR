---
title: DataControl, objet (RDS)
TOCTitle: DataControl Object (RDS)
ms:assetid: ac430669-7628-696c-c036-b5d35405d788
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249801(v=office.15)
ms:contentKeyID: 48547001
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3382b86ad14b484cb0fb9a8f6ecbd95018c25835
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25607010"
---
# <a name="datacontrol-object-rds"></a><span data-ttu-id="a089d-102">DataControl, objet (RDS)</span><span class="sxs-lookup"><span data-stu-id="a089d-102">DataControl Object (RDS)</span></span>

<span data-ttu-id="a089d-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a089d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a089d-104"><<<<<<< Tête lie un données requête [jeu d’enregistrements](recordset-object-ado.md) à un ou plusieurs contrôles (par exemple, une zone de texte, contrôle de grille ou zone de liste déroulante) pour afficher les données du **jeu d’enregistrements** dans une page Web.</span><span class="sxs-lookup"><span data-stu-id="a089d-104"><<<<<<< HEAD Binds a data query [Recordset](recordset-object-ado.md) to one or more controls (for example, a text box, grid control, or combo box) to display the **Recordset** data on a Web page.</span></span>
<span data-ttu-id="a089d-105">=== Lie un [objet Recordset](recordset-object-ado.md) de requête de données à un ou plusieurs contrôles (par exemple, une zone de texte, contrôle de grille ou zone de liste déroulante) pour afficher les données du **jeu d’enregistrements** sur une page Web.</span><span class="sxs-lookup"><span data-stu-id="a089d-105">======= Binds a data query [Recordset](recordset-object-ado.md) to one or more controls (for example, a text box, grid control, or combo box) to display the **Recordset** data on a webpage.</span></span>
>>>>>>> <span data-ttu-id="a089d-106">master</span><span class="sxs-lookup"><span data-stu-id="a089d-106">master</span></span>

## <a name="syntax"></a><span data-ttu-id="a089d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a089d-107">Syntax</span></span>

```vb
    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DataControl"
       <PARAM NAME="Connect" VALUE="DSN=DSNName;UID=usr;PWD=pw;">
       <PARAM NAME="Server" VALUE="https://awebsrvr">
       <PARAM NAME="SQL" VALUE="QueryText">
    </OBJECT>
```

## <a name="remarks"></a><span data-ttu-id="a089d-108">Notes</span><span class="sxs-lookup"><span data-stu-id="a089d-108">Remarks</span></span>

<span data-ttu-id="a089d-109">L'identificateur de classe (Class ID) de l'objet **RDS.DataControl** est BD96C556-65A3-11D0-983A-00C04FC29E33.</span><span class="sxs-lookup"><span data-stu-id="a089d-109">The class ID for the **RDS.DataControl** object is BD96C556-65A3-11D0-983A-00C04FC29E33.</span></span>

> [!NOTE]
> <span data-ttu-id="a089d-p102">[!REMARQUE] Si vous recevez un message d'erreur indiquant qu'un objet [RDS.DataSpace](dataspace-object-rds.md) ou **RDS.DataControl** ne se charge pas, vérifiez que vous utilisez le bon identificateur de classe. Les identificateurs de ces objets ont changé entre la version 1.0 et la version 1.1.</span><span class="sxs-lookup"><span data-stu-id="a089d-p102">If you get an error that an [RDS.DataSpace](dataspace-object-rds.md) or **RDS.DataControl** object doesn't load, make sure you are using the correct class ID. The class IDs for these objects have changed from version 1.0 and 1.1.</span></span>

<span data-ttu-id="a089d-112">Dans un scénario de base, il vous suffit de définir les propriétés **SQL**, **Connect** et **Server** de l'objet **RDS.DataControl**, ce qui provoquera automatiquement un appel de l'objet métier par défaut, [RDSServer.DataFactory](datafactory-object-rdsserver.md).</span><span class="sxs-lookup"><span data-stu-id="a089d-112">For a basic scenario, you need to set only the **SQL**, **Connect**, and **Server** properties of the **RDS.DataControl** object, which will automatically call the default business object, [RDSServer.DataFactory](datafactory-object-rdsserver.md).</span></span>

<span data-ttu-id="a089d-113">Toutes les propriétés de l'objet **RDS.DataControl** sont facultatives car des objets métier personnalisés peuvent remplacer leurs fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="a089d-113">All the properties in the **RDS.DataControl** are optional because custom business objects can replace their functionality.</span></span>

> [!NOTE]
> <span data-ttu-id="a089d-114">[!REMARQUE] Si votre requête porte sur des résultats multiples, seul le premier [Recordset](recordset-object-ado.md) (jeu d'enregistrements) est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="a089d-114">If you query for multiple results, only the first [Recordset](recordset-object-ado.md) is returned.</span></span> <span data-ttu-id="a089d-115">Si des jeux multiples de résultats sont nécessaires, affectez chacun d'entre eux à un **DataControl** individuel.</span><span class="sxs-lookup"><span data-stu-id="a089d-115">If multiple result sets are needed, assign each to its own **DataControl**.</span></span> 
> 
> <span data-ttu-id="a089d-116">Un exemple d’une requête de résultats multiples peut être la suivante : `"Select * from Authors, Select * from Topics"`.</span><span class="sxs-lookup"><span data-stu-id="a089d-116">An example of a query for multiple results could be the following: `"Select * from Authors, Select * from Topics"`.</span></span>

<span data-ttu-id="a089d-p104">En ajoutant « DFMode=20; » à la chaîne de connexion lorsque vous utilisez l'objet **RDS.DataControl**, vous améliorerez les performances du serveur lors de la mise à jour des données. Avec ce paramètre, l'objet **RDSServer.DataFactory** utilise moins de ressources au niveau du serveur. Toutefois, les fonctions suivantes ne sont pas disponibles dans cette configuration :</span><span class="sxs-lookup"><span data-stu-id="a089d-p104">Adding "DFMode=20;" to your connection string when using the **RDS.DataControl** object can improve your server's performance when updating data. With this setting, the **RDSServer.DataFactory** object on the server uses a less resource-intensive mode. However, the following features are not available in this configuration:</span></span>

  - <span data-ttu-id="a089d-120">utilisation de requêtes paramétrées ;</span><span class="sxs-lookup"><span data-stu-id="a089d-120">Using parameterized queries.</span></span>

  - <span data-ttu-id="a089d-121">obtention d'informations de paramètres et de colonnes avant l'appel de la méthode **Execute**;</span><span class="sxs-lookup"><span data-stu-id="a089d-121">Getting parameter or column information before calling the **Execute** method.</span></span>

  - <span data-ttu-id="a089d-122">affectation de la valeur **True** à **Transact Updates**;</span><span class="sxs-lookup"><span data-stu-id="a089d-122">Setting **Transact Updates** to **True**.</span></span>

  - <span data-ttu-id="a089d-123">obtention de l'état des lignes ;</span><span class="sxs-lookup"><span data-stu-id="a089d-123">Getting row status.</span></span>

  - <span data-ttu-id="a089d-124">appel de la méthode [Resync](resync-method-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="a089d-124">Calling the [Resync](resync-method-ado.md) method.</span></span>

  - <span data-ttu-id="a089d-125">actualisation (explicite ou automatique) via la propriété [Update Resync](update-resync-property-dynamic-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="a089d-125">Refreshing (explicitly or automatically) via the [Update Resync](update-resync-property-dynamic-ado.md) property.</span></span>

  - <span data-ttu-id="a089d-126">définition des propriétés **Command** ou [Recordset](recordset-sourcerecordset-properties-rds.md) ;</span><span class="sxs-lookup"><span data-stu-id="a089d-126">Setting **Command** or [Recordset](recordset-sourcerecordset-properties-rds.md) properties.</span></span>

  - <span data-ttu-id="a089d-127">utilisation d' **adCmdTableDirect**.</span><span class="sxs-lookup"><span data-stu-id="a089d-127">Using **adCmdTableDirect**.</span></span>

<span data-ttu-id="a089d-p105">L'objet **RDS.DataControl** s'exécute en mode asynchrone par défaut. Si l'exécution synchrone est requise pour votre application, affectez au paramètre [ExecuteOptions](executeoptions-property-rds.md) la valeur **adcExecSync** et au paramètre [FetchOptions](fetchoptions-property-rds.md) la valeur **adcFetchUpFront**, comme indiqué dans l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="a089d-p105">The **RDS.DataControl** object runs in asynchronous mode by default. If you require synchronous execution for your application, set the [ExecuteOptions](executeoptions-property-rds.md) parameter equal to **adcExecSync** and the [FetchOptions](fetchoptions-property-rds.md) parameter equal to **adcFetchUpFront**, as shown in the following example.</span></span>

```vb
    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
        ID="DataControl"
       <PARAM NAME="Connect" VALUE="DSN=DSNName;UID=usr;PWD=pw;">
       <PARAM NAME="Server" VALUE="https://awebsrvr">
       <PARAM NAME="SQL" VALUE="QueryText">
       <PARAM NAME="ExecuteOptions" VALUE="1">
       <PARAM NAME="FetchOptions" VALUE="1">
    </OBJECT>
```

<span data-ttu-id="a089d-p106">Utilisez un objet **RDS.DataControl** pour lier les résultats d'une seule requête à un ou plusieurs contrôles visuels. Par exemple, supposons que vous écriviez une requête visant à obtenir des données client comme le nom, l'adresse, le lieu de naissance, l'âge et le statut prioritaire du client. Vous pouvez utiliser un seul objet **RDS.DataControl** pour afficher le nom, l'âge et la région dans trois zones de texte distinctes, le statut prioritaire sous la forme d'une case à cocher et toutes les données dans un contrôle de grille.</span><span class="sxs-lookup"><span data-stu-id="a089d-p106">Use one **RDS.DataControl** object to link the results of a single query to one or more visual controls. For example, suppose you code a query requesting customer data such as Name, Residence, Place of Birth, Age, and Priority Customer Status. You can use a single **RDS.DataControl** object to display a customer's Name, Age, and Region in three separate text boxes; Priority Customer Status in a check box; and all the data in a grid control.</span></span>

<span data-ttu-id="a089d-p107">Utilisez des objets **RDS.DataControl** différents pour lier les résultats de requêtes multiples à des contrôles visuels distincts. Supposons par exemple que vous utilisiez une requête pour obtenir des informations sur un client et une deuxième requête pour obtenir des informations sur les articles achetés par ce client. Vous voulez afficher les résultats de la première requête dans trois zones de texte et à l'aide d'une case à cocher, et ceux de la deuxième requête dans un contrôle de grille. Si vous utilisez l'objet métier par défaut (**RDSServer.DataFactory**), vous devez procéder comme suit :</span><span class="sxs-lookup"><span data-stu-id="a089d-p107">Use different **RDS.DataControl** objects to link the results of multiple queries to different visual controls. For example, suppose you use one query to obtain information about a customer, and a second query to obtain information about merchandise that the customer has purchased. You want to display the results of the first query in three text boxes and one check box, and the results of the second query in a grid control. If you use the default business object (**RDSServer.DataFactory**), you need to do the following:</span></span>

<span data-ttu-id="a089d-137"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="a089d-137"><<<<<<< HEAD</span></span>
  - <span data-ttu-id="a089d-138">Ajouter deux objets **RDS.DataControl** à votre page Web.</span><span class="sxs-lookup"><span data-stu-id="a089d-138">Add two **RDS.DataControl** objects to your Web page.</span></span>
=======
  - <span data-ttu-id="a089d-139">Ajoutez deux **RDS. DataControl** objets à votre page Web.</span><span class="sxs-lookup"><span data-stu-id="a089d-139">Add two **RDS.DataControl** objects to your webpage.</span></span>
>>>>>>> <span data-ttu-id="a089d-140">master</span><span class="sxs-lookup"><span data-stu-id="a089d-140">master</span></span>

  - <span data-ttu-id="a089d-p108">Rédiger deux requêtes, une pour chaque propriété **SQL** des deux objets **RDS.DataControl**. Un objet **RDS.DataControl** contiendra une requête SQL demandant des informations client ; le deuxième objet contiendra une requête demandant la liste des articles achetés par le client.</span><span class="sxs-lookup"><span data-stu-id="a089d-p108">Write two queries, one for each **SQL** property of the two **RDS.DataControl** objects. One **RDS.DataControl** object will contain an SQL query requesting customer information; the second will contain a query requesting a list of merchandise the customer has purchased.</span></span>

  - <span data-ttu-id="a089d-143">Dans chaque balise OBJECT des contrôles liés, indiquez la valeur DATAFLD pour définir les valeurs des données à afficher dans chaque contrôle visuel.</span><span class="sxs-lookup"><span data-stu-id="a089d-143">In each of the bound controls' OBJECT tags, specify the DATAFLD value to set the values for the data you want to display in each visual control.</span></span>

<span data-ttu-id="a089d-144"><<<<<<< Tête il n’existe aucune restriction de comptage du nombre de **RDS. DataControl** objets que vous pouvez imbriquer via des balises OBJECT dans une page Web unique.</span><span class="sxs-lookup"><span data-stu-id="a089d-144"><<<<<<< HEAD There is no count restriction on the number of **RDS.DataControl** objects that you can embed via OBJECT tags on a single Web page.</span></span>

<a name="when-you-define-the-rdsdatacontrol-object-on-a-web-page-use-nonzero-height-and-width-values-such-as-1-to-avoid-the-inclusion-of-extra-space"></a><span data-ttu-id="a089d-145">Lorsque vous définissez l'objet **RDS.DataControl** dans une page Web, utilisez des valeurs différentes de zéro pour **Height** et **Width**, telles que 1 (pour éviter d'inclure des espaces inutiles).</span><span class="sxs-lookup"><span data-stu-id="a089d-145">When you define the **RDS.DataControl** object on a Web page, use nonzero **Height** and **Width** values such as 1 (to avoid the inclusion of extra space).</span></span>
=======
<span data-ttu-id="a089d-146">Il n’existe aucune restriction de comptage du nombre de **RDS. DataControl** objets que vous pouvez imbriquer via des balises OBJECT dans une seule page Web.</span><span class="sxs-lookup"><span data-stu-id="a089d-146">There is no count restriction on the number of **RDS.DataControl** objects that you can embed via OBJECT tags on a single webpage.</span></span>

<span data-ttu-id="a089d-147">Lorsque vous définissez la **RDS. DataControl** d’objets sur une page Web, utilisez des valeurs différentes de zéro de **hauteur** et la **largeur** tel que 1 (pour éviter d’inclure des espaces inutiles).</span><span class="sxs-lookup"><span data-stu-id="a089d-147">When you define the **RDS.DataControl** object on a webpage, use nonzero **Height** and **Width** values such as 1 (to avoid the inclusion of extra space).</span></span>
>>>>>>> <span data-ttu-id="a089d-148">master</span><span class="sxs-lookup"><span data-stu-id="a089d-148">master</span></span>

<span data-ttu-id="a089d-149">Les composants clients Remote Data Service sont déjà inclus dans Internet Explorer 4.0 ; vous n'avez donc pas besoin d'inclure un paramètre CODEBASE dans votre balise d'objet **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="a089d-149">Remote Data Service client components are already included as part of Internet Explorer 4.0; therefore, you don't need to include a CODEBASE parameter in your **RDS.DataControl** object tag.</span></span>

<span data-ttu-id="a089d-150">Avec Internet Explorer 4.0 ou version ultérieure, vous pouvez effectuer une liaison à des données à l'aide de contrôles HTML et ActiveX® uniquement s'ils sont identifiés comme des contrôles de modèle cloisonné.</span><span class="sxs-lookup"><span data-stu-id="a089d-150">With Internet Explorer 4.0 or later, you can bind to data by using HTML controls and ActiveX® controls only if they are marked as apartment model controls.</span></span>

<span data-ttu-id="a089d-151">**Utilisateurs de Microsoft Visual Basic** **RDS. DataControl** est utilisé uniquement dans les applications Web.</span><span class="sxs-lookup"><span data-stu-id="a089d-151">**Microsoft Visual Basic Users** The **RDS.DataControl** is used only in web-based applications.</span></span> <span data-ttu-id="a089d-152">Les applications clientes Visual Basic n'en ont pas besoin.</span><span class="sxs-lookup"><span data-stu-id="a089d-152">A Visual Basic client application has no need for it.</span></span>

