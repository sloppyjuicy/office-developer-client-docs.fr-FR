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
# <a name="work-with-digital-signatures-using-the-infopath-2003-object-model"></a>Utiliser des signatures numériques à l’aide du modèle objet InfoPath 2003

Le modèle objet compatible avec InfoPath 2003 propose des fonctionnalités qui permettent l'utilisation de signatures numériques par programme.
  
## <a name="digital-signature-features"></a>Fonctionnalités de signature numérique

Les fonctionnalités de signature numérique disponibles dans InfoPath vous permettent de : 
  
- activer les signatures pour l'ensemble du formulaire ou pour des jeux de données spécifiques à signer séparément dans le formulaire ;
    
- préciser, pour chaque jeu de données pouvant être signé, si une ou plusieurs signatures sont autorisées et quelles seront leurs relations. Par exemple, vous pouvez spécifier s'il s'agit de co-signatures parallèles ou si chaque nouvelle signature contre-signe toutes les signatures précédentes ;
    
- définir un message à présenter aux utilisateurs du formulaire lorsqu'ils signent le formulaire ;
    
- insérer et afficher une signature dans le document ; 
    
- afficher des informations vérifiables de non-répudiation ajoutées à chaque signature pour une plus grande sécurité. Ces informations supplémentaires, qui comprennent une vue du formulaire tel qu'il est présenté à chaque signataire, font partie de la signature et ne peuvent pas en être supprimées sans annuler la signature. Vous pouvez à tout moment revoir ces données en cliquant sur la signature dans le formulaire pour afficher la boîte de dialogue **Vérifier la signature numérique**; 
    
- tirer parti d'un modèle objet permettant l'utilisation de signatures numériques et ajouter des informations personnalisées au bloc de signatures dans les formulaires entièrement fiables via un modèle objet de signature numérique. 
    
## <a name="overview-of-the-digital-signatures-object-model"></a>Présentation du modèle objet des signatures numériques

### <a name="events"></a>Événements

Le modèle objet des signatures numériques fournit l'événement qui suit.
  
|**Name**|**Description**|
|:-----|:-----|
|[OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx) <br/> |Se produit une fois qu'un ensemble de données à signer a été sélectionné pour une signature.  <br/> Vous pouvez utiliser cet événement pour manipuler les données stockées dans la signature numérique. Par exemple, vous pouvez ajouter les données d'un serveur d'horodatage fiable ou une contre-signature côté serveur de la transaction. Vous pouvez également utiliser cet événement pour bloquer la signature si l'utilisateur actuel n'est pas membre d'un groupe spécifique.  <br/> |
   
L'événement **OnSign** renvoie une référence à l'objet [SignEventObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEventObject.aspx) , qui fournit les propriétés suivantes. 
  
|**Name**|**Description**|
|:-----|:-----|
|[ReturnStatus](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SignEvent.ReturnStatus.aspx) <br/> |Récupère ou définit une valeur **Boolean** (booléenne) indiquant l'état de retour de l'événement **OnSign**.  <br/> |
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SignEvent.SignedDataBlock.aspx) <br/> |Récupère le bloc de données signées qui a déclenché l'événement **OnSign**.  <br/> |
|[XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.XDocument.aspx) <br/> |Récupère une référence à l'objet **XDocument** associé à l'événement **OnSign**.  <br/> |
   
### <a name="collections-and-objects"></a>Collections et objets

Le modèle objet des signatures numériques fournit les collections suivantes.
  
|**Name**|**Description**|
|:-----|:-----|
|[SignedDataBlocksCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlocksCollection.aspx) <br/> |Collection des objets [SignedDataBlockObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) dans le modèle de formulaire tel que défini dans le fichier de définition du formulaire (.xsf).  <br/> La collection **SignedDataBlocksCollection** implémente des propriétés qui permettent d'accéder aux objets **SignedDataBlockObjects** associés à un formulaire. La collection **SignedDataBlocks est** accessible via la propriété [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SignedDataBlocks.aspx) de l’objet [XDocument.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx)  <br/> |
|[SignaturesCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignaturesCollection.aspx) <br/> |Contient une collection [d’objets SignatureObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) pour **chaque objet SignedDataBlockObject** du formulaire.  <br/> La collection **SignaturesCollection** implémente des propriétés et une méthode qui permettent d'accéder aux objets **SignatureObject** associés au formulaire et de créer une signature. Cette collection est accessible via l'objet **SignedDataBlockObject**. <br/> Lorsque vous utilisez la méthode [Create](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signatures.Create.aspx) de la collection **SignaturesCollection,** n’oubliez pas que la signature n’est pas écrite tant que la méthode [Sign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) n’est pas appelée sur l’objet **SignatureObject.** Ces méthodes peuvent être appelées uniquement depuis le gestionnaire d'événements **OnSign** d'un modèle de formulaire avec confiance totale.  <br/> |
   
Le modèle objet des signatures numériques fournit les objets suivants.
  
|**Name**|**Description**|
|:-----|:-----|
|[SignedDataBlockObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) <br/> |Représente un ensemble de données à signer dans un formulaire. L'objet **SignedDataBlock** fournit une méthode et un certain nombre de propriétés qui peuvent être utilisées pour interagir par programme avec un ensemble de données à signer.<br/> |
|[SignatureObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) <br/> |Représente une signature numérique qui a été ajoutée à un formulaire ou à un ensemble de données signables dans un formulaire. La collection **SignatureObject** implémente des propriétés qui peuvent être utilisées pour récupérer des informations sur la signature numérique et la méthode [Sign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) pour écrire le bloc de signature numérique XML et calculer sa valeur de hachage de chiffrement.  <br/> |
|[CertificateObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.CertificateObject.aspx) <br/> |Représente le certificat numérique X.509 utilisé pour créer la signature.  <br/> |
   
## <a name="working-with-digital-signatures-programmatically"></a>Utilisation de signatures numériques par programme

Le modèle objet compatible avec InfoPath 2003 fournit les membres permettant d'agir par programme sur les signatures numériques. Plus spécifiquement, les formulaires avec confiance totale peuvent ajouter des informations personnalisées au bloc de signature avant sa validation, selon la séquence qui suit :
  
1. L'utilisateur choisit d'ajouter une signature numérique à un formulaire.
    
2. La première fenêtre de l' **Assistant Signature numérique** s'affiche. 
    
3. L'événement **OnSign** des données sélectionnées, représentées par l'objet **SignedDataBlockObject**, est déclenché et la méthode **Sign** de **SignedDataBlockObject** et la méthode **Create** de la collection **SignaturesCollection** s'exécutent. 
    
4. Les actions personnalisées facultatives sont exécutées.
    
5. La méthode **Sign** de **SignatureObject** s'exécute. 
    
6. Les deuxième et troisième fenêtres de l'Assistant s'affichent pour le choix du certificat de signature et la saisie de commentaires.
    
7. Les informations de non-répudiation s'affichent. (Elles peuvent être consultées ultérieurement dans la boîte de dialogue **Vérifier la signature numérique**.) 
    
8. Lorsque l'utilisateur clique sur le bouton **Signer**, la signature est ajoutée à la collection de signatures du formulaire. 
    
L'exemple qui suit appelle la boîte de dialogue **Signer** et contre-signe la signature avec une valeur d'horodatage obtenue auprès d'un service d'horodatage approuvé. 
  
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


