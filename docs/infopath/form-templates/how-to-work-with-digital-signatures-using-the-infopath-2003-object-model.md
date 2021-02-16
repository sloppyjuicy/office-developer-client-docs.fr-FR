---
title: Utiliser des signatures numériques à l’aide du modèle objet InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- digital signatures [infopath 2007], infopath 2003-compatible form templates,InfoPath 2003-compatible form templates, digital signatures
localization_priority: Normal
ms.assetid: d6318238-fd45-4854-a3c9-c27c5685bd6b
description: Le modèle objet compatible avec InfoPath 2003 propose des fonctionnalités qui permettent l'utilisation de signatures numériques par programme.
ms.openlocfilehash: 86e2c85c7515c896612df09b6186462480ceff61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433443"
---
# <a name="work-with-digital-signatures-using-the-infopath-2003-object-model"></a><span data-ttu-id="fe3b3-104">Utiliser des signatures numériques à l’aide du modèle objet InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="fe3b3-104">Work with Digital Signatures Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="fe3b3-105">Le modèle objet compatible avec InfoPath 2003 propose des fonctionnalités qui permettent l'utilisation de signatures numériques par programme.</span><span class="sxs-lookup"><span data-stu-id="fe3b3-105">The InfoPath 2003-compatible object model provides features for working with digital signatures programmatically.</span></span>
  
## <a name="digital-signature-features"></a><span data-ttu-id="fe3b3-106">Fonctionnalités de signature numérique</span><span class="sxs-lookup"><span data-stu-id="fe3b3-106">Digital Signature Features</span></span>

<span data-ttu-id="fe3b3-107">Les fonctionnalités de signature numérique disponibles dans InfoPath vous permettent de :</span><span class="sxs-lookup"><span data-stu-id="fe3b3-107">The digital signatures features available in InfoPath enable you to:</span></span> 
  
- <span data-ttu-id="fe3b3-108">activer les signatures pour l'ensemble du formulaire ou pour des jeux de données spécifiques à signer séparément dans le formulaire ;</span><span class="sxs-lookup"><span data-stu-id="fe3b3-108">Enable signatures for the entire form, or for specific sets of data in the form that can be signed separately.</span></span>
    
- <span data-ttu-id="fe3b3-p101">préciser, pour chaque jeu de données pouvant être signé, si une ou plusieurs signatures sont autorisées et quelles seront leurs relations. Par exemple, vous pouvez spécifier s'il s'agit de co-signatures parallèles ou si chaque nouvelle signature contre-signe toutes les signatures précédentes ;</span><span class="sxs-lookup"><span data-stu-id="fe3b3-p101">Specify, for each set of data that can be signed, whether a single signature or multiple signatures are allowed and what their relationship will be. For example, you can specify whether they are parallel co-signatures or whether each new signature countersigns all the earlier signatures.</span></span>
    
- <span data-ttu-id="fe3b3-111">définir un message à présenter aux utilisateurs du formulaire lorsqu'ils signent le formulaire ;</span><span class="sxs-lookup"><span data-stu-id="fe3b3-111">Specify a message to be shown to form users as they sign the form.</span></span>
    
- <span data-ttu-id="fe3b3-112">insérer et afficher une signature dans le document ;</span><span class="sxs-lookup"><span data-stu-id="fe3b3-112">Insert and see a signature in the document.</span></span> 
    
- <span data-ttu-id="fe3b3-p102">afficher des informations vérifiables de non-répudiation ajoutées à chaque signature pour une plus grande sécurité. Ces informations supplémentaires, qui comprennent une vue du formulaire tel qu'il est présenté à chaque signataire, font partie de la signature et ne peuvent pas en être supprimées sans annuler la signature. Vous pouvez à tout moment revoir ces données en cliquant sur la signature dans le formulaire pour afficher la boîte de dialogue **Vérifier la signature numérique**;</span><span class="sxs-lookup"><span data-stu-id="fe3b3-p102">View verifiable non-repudiation information that has been added to each signature for increased security. This additional information, which includes a view of the form as it was presented to each signer, is part of the signature and cannot be removed without invalidating the signature. At any time, you can recall this data by clicking on the signature in the form to display the **Verify Digital Signature** dialog box.</span></span> 
    
- <span data-ttu-id="fe3b3-p103">tirer parti d'un modèle objet permettant l'utilisation de signatures numériques et ajouter des informations personnalisées au bloc de signatures dans les formulaires entièrement fiables via un modèle objet de signature numérique.</span><span class="sxs-lookup"><span data-stu-id="fe3b3-p103">Take advantage of an object model for working with digital signatures. Add custom information to the signature block in fully trusted forms through the digital signature object model.</span></span> 
    
## <a name="overview-of-the-digital-signatures-object-model"></a><span data-ttu-id="fe3b3-118">Présentation du modèle objet des signatures numériques</span><span class="sxs-lookup"><span data-stu-id="fe3b3-118">Overview of the Digital Signatures Object Model</span></span>

### <a name="events"></a><span data-ttu-id="fe3b3-119">Événements</span><span class="sxs-lookup"><span data-stu-id="fe3b3-119">Events</span></span>

<span data-ttu-id="fe3b3-120">Le modèle objet des signatures numériques fournit l'événement qui suit.</span><span class="sxs-lookup"><span data-stu-id="fe3b3-120">The object model for digital signatures provides the following event.</span></span>
  
|<span data-ttu-id="fe3b3-121">**Name**</span><span class="sxs-lookup"><span data-stu-id="fe3b3-121">**Name**</span></span>|<span data-ttu-id="fe3b3-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="fe3b3-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fe3b3-123">OnSign</span><span class="sxs-lookup"><span data-stu-id="fe3b3-123">OnSign</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx) <br/> |<span data-ttu-id="fe3b3-124">Se produit une fois qu'un ensemble de données à signer a été sélectionné pour une signature.</span><span class="sxs-lookup"><span data-stu-id="fe3b3-124">Occurs after a set of signable data has been selected to sign.</span></span>  <br/> <span data-ttu-id="fe3b3-p104">Vous pouvez utiliser cet événement pour manipuler les données stockées dans la signature numérique. Par exemple, vous pouvez ajouter les données d'un serveur d'horodatage fiable ou une contre-signature côté serveur de la transaction. Vous pouvez également utiliser cet événement pour bloquer la signature si l'utilisateur actuel n'est pas membre d'un groupe spécifique.</span><span class="sxs-lookup"><span data-stu-id="fe3b3-p104">You can use this event to manipulate the data stored within the digital signature. For example, you can add data from a trusted timestamp server, or add a server-side countersignature of the transaction. You can also use this event to block signing if the current user is not a member of a particular group.</span></span>  <br/> |
   
<span data-ttu-id="fe3b3-128">L'événement **OnSign** renvoie une référence à l'objet [SignEventObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEventObject.aspx) , qui fournit les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="fe3b3-128">The **OnSign** event returns a reference to the [SignEventObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEventObject.aspx) object, which provides the following properties.</span></span> 
  
|<span data-ttu-id="fe3b3-129">**Name**</span><span class="sxs-lookup"><span data-stu-id="fe3b3-129">**Name**</span></span>|<span data-ttu-id="fe3b3-130">**Description**</span><span class="sxs-lookup"><span data-stu-id="fe3b3-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fe3b3-131">ReturnStatus</span><span class="sxs-lookup"><span data-stu-id="fe3b3-131">ReturnStatus</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SignEvent.ReturnStatus.aspx) <br/> |<span data-ttu-id="fe3b3-132">Récupère ou définit une valeur **Boolean** (booléenne) indiquant l'état de retour de l'événement **OnSign**.</span><span class="sxs-lookup"><span data-stu-id="fe3b3-132">Gets or sets a **Boolean** value indicating the return status of the **OnSign** event.</span></span>  <br/> |
|[<span data-ttu-id="fe3b3-133">SignedDataBlock</span><span class="sxs-lookup"><span data-stu-id="fe3b3-133">SignedDataBlock</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SignEvent.SignedDataBlock.aspx) <br/> |<span data-ttu-id="fe3b3-134">Récupère le bloc de données signées qui a déclenché l'événement **OnSign**.</span><span class="sxs-lookup"><span data-stu-id="fe3b3-134">Gets the signed data block that triggered the **OnSign** event.</span></span>  <br/> |
|[<span data-ttu-id="fe3b3-135">XDocument</span><span class="sxs-lookup"><span data-stu-id="fe3b3-135">XDocument</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.XDocument.aspx) <br/> |<span data-ttu-id="fe3b3-136">Récupère une référence à l'objet **XDocument** associé à l'événement **OnSign**.</span><span class="sxs-lookup"><span data-stu-id="fe3b3-136">Gets a reference to the **XDocument** object associated with the **OnSign** event.</span></span>  <br/> |
   
### <a name="collections-and-objects"></a><span data-ttu-id="fe3b3-137">Collections et objets</span><span class="sxs-lookup"><span data-stu-id="fe3b3-137">Collections and Objects</span></span>

<span data-ttu-id="fe3b3-138">Le modèle objet des signatures numériques fournit les collections suivantes.</span><span class="sxs-lookup"><span data-stu-id="fe3b3-138">The object model for digital signatures provides the following collections.</span></span>
  
|<span data-ttu-id="fe3b3-139">**Name**</span><span class="sxs-lookup"><span data-stu-id="fe3b3-139">**Name**</span></span>|<span data-ttu-id="fe3b3-140">**Description**</span><span class="sxs-lookup"><span data-stu-id="fe3b3-140">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fe3b3-141">SignedDataBlocksCollection</span><span class="sxs-lookup"><span data-stu-id="fe3b3-141">SignedDataBlocksCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlocksCollection.aspx) <br/> |<span data-ttu-id="fe3b3-142">Collection des objets [SignedDataBlockObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) dans le modèle de formulaire tel que défini dans le fichier de définition du formulaire (.xsf).</span><span class="sxs-lookup"><span data-stu-id="fe3b3-142">The collection of the [SignedDataBlockObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) objects in the form template as defined in the form definition file (.xsf).</span></span>  <br/> <span data-ttu-id="fe3b3-143">La collection **SignedDataBlocksCollection** implémente des propriétés qui permettent d'accéder aux objets **SignedDataBlockObjects** associés à un formulaire.</span><span class="sxs-lookup"><span data-stu-id="fe3b3-143">The **SignedDataBlocksCollection** collection implements properties that can be used to access the **SignedDataBlockObjects** objects associated with a form.</span></span> <span data-ttu-id="fe3b3-144">La collection **SignedDataBlocks est** accessible via la propriété [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SignedDataBlocks.aspx) de l’objet [XDocument.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx)</span><span class="sxs-lookup"><span data-stu-id="fe3b3-144">The **SignedDataBlocks** collection is accessible through the [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SignedDataBlocks.aspx) property of the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) object.</span></span>  <br/> |
|[<span data-ttu-id="fe3b3-145">SignaturesCollection</span><span class="sxs-lookup"><span data-stu-id="fe3b3-145">SignaturesCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignaturesCollection.aspx) <br/> |<span data-ttu-id="fe3b3-146">Contient une collection [d’objets SignatureObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) pour **chaque objet SignedDataBlockObject** du formulaire.</span><span class="sxs-lookup"><span data-stu-id="fe3b3-146">Contains a collection of [SignatureObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) objects for each **SignedDataBlockObject** in the form.</span></span>  <br/> <span data-ttu-id="fe3b3-147">La collection **SignaturesCollection** implémente des propriétés et une méthode qui permettent d'accéder aux objets **SignatureObject** associés au formulaire et de créer une signature.</span><span class="sxs-lookup"><span data-stu-id="fe3b3-147">The **SignaturesCollection** collection implements properties and a method that can be used to access a form's associated **SignatureObject** objects and to create a signature.</span></span> <span data-ttu-id="fe3b3-148">Cette collection est accessible via l'objet **SignedDataBlockObject**.</span><span class="sxs-lookup"><span data-stu-id="fe3b3-148">It is accessible through the **SignedDataBlockObject** object.</span></span>  <br/> <span data-ttu-id="fe3b3-149">Lorsque vous utilisez la méthode [Create](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signatures.Create.aspx) de la collection **SignaturesCollection,** n’oubliez pas que la signature n’est pas écrite tant que la méthode [Sign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) n’est pas appelée sur l’objet **SignatureObject.**</span><span class="sxs-lookup"><span data-stu-id="fe3b3-149">When you use the [Create](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signatures.Create.aspx) method of the **SignaturesCollection** collection, keep in mind that the signature is not written until the [Sign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) method is called on the **SignatureObject** object.</span></span> <span data-ttu-id="fe3b3-150">Ces méthodes peuvent être appelées uniquement depuis le gestionnaire d'événements **OnSign** d'un modèle de formulaire avec confiance totale.</span><span class="sxs-lookup"><span data-stu-id="fe3b3-150">These methods can be called only from the **OnSign** event handler of a fully trusted form template.</span></span>  <br/> |
   
<span data-ttu-id="fe3b3-151">Le modèle objet des signatures numériques fournit les objets suivants.</span><span class="sxs-lookup"><span data-stu-id="fe3b3-151">The object model for digital signatures provides the following objects.</span></span>
  
|<span data-ttu-id="fe3b3-152">**Name**</span><span class="sxs-lookup"><span data-stu-id="fe3b3-152">**Name**</span></span>|<span data-ttu-id="fe3b3-153">**Description**</span><span class="sxs-lookup"><span data-stu-id="fe3b3-153">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fe3b3-154">SignedDataBlockObject</span><span class="sxs-lookup"><span data-stu-id="fe3b3-154">SignedDataBlockObject</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) <br/> |<span data-ttu-id="fe3b3-155">Représente un ensemble de données à signer dans un formulaire.</span><span class="sxs-lookup"><span data-stu-id="fe3b3-155">Represents a set of signable data in a form.</span></span> <span data-ttu-id="fe3b3-156">L'objet **SignedDataBlock** fournit une méthode et un certain nombre de propriétés qui peuvent être utilisées pour interagir par programme avec un ensemble de données à signer.</span><span class="sxs-lookup"><span data-stu-id="fe3b3-156">The **SignedDataBlock** object provides a number of properties and one method that can be used to programmatically interact with a set of signable data.</span></span>  <br/> |
|[<span data-ttu-id="fe3b3-157">SignatureObject</span><span class="sxs-lookup"><span data-stu-id="fe3b3-157">SignatureObject</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) <br/> |<span data-ttu-id="fe3b3-158">Représente une signature numérique qui a été ajoutée à un formulaire ou à un ensemble de données signables dans un formulaire.</span><span class="sxs-lookup"><span data-stu-id="fe3b3-158">Represents a digital signature that has been added to a form or set of signable data in a form.</span></span> <span data-ttu-id="fe3b3-159">La collection **SignatureObject** implémente des propriétés qui peuvent être utilisées pour récupérer des informations sur la signature numérique et la méthode [Sign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) pour écrire le bloc de signature numérique XML et calculer sa valeur de hachage de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="fe3b3-159">The **SignatureObject** collection implements properties that can be used to retrieve information about the digital signature, and the [Sign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) method for writing the XML digital signature block and computing its cryptographic hash value.</span></span>  <br/> |
|[<span data-ttu-id="fe3b3-160">CertificateObject</span><span class="sxs-lookup"><span data-stu-id="fe3b3-160">CertificateObject</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.CertificateObject.aspx) <br/> |<span data-ttu-id="fe3b3-161">Représente le certificat numérique X.509 utilisé pour créer la signature.</span><span class="sxs-lookup"><span data-stu-id="fe3b3-161">Represents the X.509 digital certificate that has been used to create the signature.</span></span>  <br/> |
   
## <a name="working-with-digital-signatures-programmatically"></a><span data-ttu-id="fe3b3-162">Utilisation de signatures numériques par programme</span><span class="sxs-lookup"><span data-stu-id="fe3b3-162">Working with Digital Signatures Programmatically</span></span>

<span data-ttu-id="fe3b3-p110">Le modèle objet compatible avec InfoPath 2003 fournit les membres permettant d'agir par programme sur les signatures numériques. Plus spécifiquement, les formulaires avec confiance totale peuvent ajouter des informations personnalisées au bloc de signature avant sa validation, selon la séquence qui suit :</span><span class="sxs-lookup"><span data-stu-id="fe3b3-p110">The InfoPath 2003-compatible object model provides members for interacting with digital signatures programmatically. In particular, fully-trusted forms can add custom information to the signature block before it is committed, according to the following timeline:</span></span>
  
1. <span data-ttu-id="fe3b3-165">L'utilisateur choisit d'ajouter une signature numérique à un formulaire.</span><span class="sxs-lookup"><span data-stu-id="fe3b3-165">User chooses to add a digital signature to a form.</span></span>
    
2. <span data-ttu-id="fe3b3-166">La première fenêtre de l' **Assistant Signature numérique** s'affiche.</span><span class="sxs-lookup"><span data-stu-id="fe3b3-166">The first panel of the **Digital Signature Wizard** is displayed.</span></span> 
    
3. <span data-ttu-id="fe3b3-167">L'événement **OnSign** des données sélectionnées, représentées par l'objet **SignedDataBlockObject**, est déclenché et la méthode **Sign** de **SignedDataBlockObject** et la méthode **Create** de la collection **SignaturesCollection** s'exécutent.</span><span class="sxs-lookup"><span data-stu-id="fe3b3-167">The **OnSign** event for the selected data represented by the **SignedDataBlockObject** object is raised, and the **Sign** method of **SignedDataBlockObject** and the **Create** method of the **SignaturesCollection** collection are executed.</span></span> 
    
4. <span data-ttu-id="fe3b3-168">Les actions personnalisées facultatives sont exécutées.</span><span class="sxs-lookup"><span data-stu-id="fe3b3-168">Any optional custom actions are executed.</span></span>
    
5. <span data-ttu-id="fe3b3-169">La méthode **Sign** de **SignatureObject** s'exécute.</span><span class="sxs-lookup"><span data-stu-id="fe3b3-169">The **Sign** method of the **SignatureObject** is executed.</span></span> 
    
6. <span data-ttu-id="fe3b3-170">Les deuxième et troisième fenêtres de l'Assistant s'affichent pour le choix du certificat de signature et la saisie de commentaires.</span><span class="sxs-lookup"><span data-stu-id="fe3b3-170">Second and third panes of the wizard are displayed for selecting a certificate to sign with and to enter comments.</span></span>
    
7. <span data-ttu-id="fe3b3-171">Les informations de non-répudiation s'affichent. (Elles peuvent être consultées ultérieurement dans la boîte de dialogue **Vérifier la signature numérique**.)</span><span class="sxs-lookup"><span data-stu-id="fe3b3-171">The non-repudiation information is displayed (which can be viewed later with the **Verify Digital Signature** dialog box).</span></span> 
    
8. <span data-ttu-id="fe3b3-172">Lorsque l'utilisateur clique sur le bouton **Signer**, la signature est ajoutée à la collection de signatures du formulaire.</span><span class="sxs-lookup"><span data-stu-id="fe3b3-172">When the **Sign** button is clicked, the signature is added to collection of signatures for the form.</span></span> 
    
<span data-ttu-id="fe3b3-173">L'exemple qui suit appelle la boîte de dialogue **Signer** et contre-signe la signature avec une valeur d'horodatage obtenue auprès d'un service d'horodatage approuvé.</span><span class="sxs-lookup"><span data-stu-id="fe3b3-173">The following example invokes the **Sign** dialog box and countersigns the signature with a timestamp value retrieved from a trusted timestamp service.</span></span> 
  
```cs
[InfoPathEventHandler(EventType=InfoPathEventType.OnSign)]
public void OnSign(SignEvent e)
{
    Signature signature = e.SignedDataBlock.Signatures.Create();
    // Invoke the Sign dialog box to sign the data block.
    signature.Sign();
    // Countersign the signature with a trusted timestamp
    // Get the XML node storing the signature block
    IXMLDOMNode oNodeSig = signature.SignatureBlockXmlNode;
    IXMLDOMNode oNodeSigValue = oNodeSig.selectSingleNode(".//*[local-name(.)='signatureValue']");
    // Get timestamp from a trusted timestamp service (fictitious).
    MyTrustedTimeStampService s = new MyTrustedTimeStampService();
    string strVerifiedTimeStamp = s.AddTimeStamp(oNodeSigValue.text);
    
    //Add the value returned from the timestamp service to the 
    //unsigned part of the signature block
    IXMLDOMNode oNodeObj = oNodeSig.selectSingleNode(".//*[local-name(.)='Object']");
    IXMLDOMNode oNode = oNodeObj.cloneNode(false);
    oNode.text = strVerifiedTimeStamp;
    oNodeObj.parentNode.appendChild(oNode);
    e.ReturnStatus = true;
}
```


