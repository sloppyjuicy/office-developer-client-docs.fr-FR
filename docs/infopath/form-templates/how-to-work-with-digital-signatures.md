---
title: Travailler avec des signatures numériques
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- digital signatures [infopath 2007],InfoPath 2007, digital signatures
ms.localizationpriority: medium
ms.assetid: fd13fb71-aecf-47bb-8a6b-db70bd90ceeb
description: Le modèle objet de l'espace de noms Microsoft.Office.InfoPath fournit les fonctionnalités d'utilisation des signatures numériques par programmation.
ms.openlocfilehash: 623ddf61f8f61c39d83247c6a19b34a0c40afcc3
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62773767"
---
# <a name="work-with-digital-signatures"></a>Travailler avec des signatures numériques

Le modèle objet de l'espace de noms [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) fournit les fonctionnalités d'utilisation des signatures numériques par programmation. 
  
## <a name="digital-signature-features"></a>Fonctionnalités de signature numérique

Les fonctionnalités de signature numérique fournies par InfoPath vous permettent d'effectuer les opérations suivantes : 
  
- activer les signatures pour l'ensemble du formulaire ou pour des jeux de données spécifiques à signer séparément dans le formulaire ;
    
- préciser, pour chaque jeu de données pouvant être signé, si une ou plusieurs signatures sont autorisées et quelles seront leurs relations. Par exemple, vous pouvez spécifier s'il s'agit de co-signatures parallèles ou si chaque nouvelle signature contre-signe toutes les signatures précédentes ;
    
- définir un message à présenter aux utilisateurs du formulaire lorsqu'ils signent le formulaire ;
    
- insérer et afficher une signature dans le document ; 
    
- afficher des informations vérifiables de non-répudiation ajoutées à chaque signature pour une plus grande sécurité. Ces informations supplémentaires, qui comprennent une vue du formulaire tel qu'il est présenté à chaque signataire, font partie de la signature et ne peuvent pas en être supprimées sans annuler la signature. Vous pouvez à tout moment revoir ces données en cliquant sur la signature dans le formulaire pour afficher la boîte de dialogue **Vérifier la signature numérique**; 
    
- tirer parti d'un modèle objet permettant l'utilisation de signatures numériques et ajouter des informations personnalisées au bloc de signatures dans les formulaires entièrement fiables via un modèle objet de signature numérique. 
    
## <a name="overview-of-the-digital-signatures-object-model"></a>Présentation du modèle objet de signatures numériques

### <a name="the-sign-event"></a>Événement Signature (Sign)

Le modèle objet des signatures numériques fournit l'événement qui suit.
  
|**Name**|**Description**|
|:-----|:-----|
|[Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) <br/> |Se produit une fois qu'un ensemble de données a été sélectionné pour la signature. Vous pouvez utiliser cet événement pour manipuler les données stockées dans la signature numérique. Par exemple, vous pouvez ajouter les données d'un serveur d'horodatage fiable ou une contre-signature côté serveur de la transaction. Vous pouvez également utiliser cet événement pour bloquer la signature si l'utilisateur actuel n'est pas membre d'un groupe spécifique. |
   
### <a name="the-signeventargs-object"></a>Objet SignEventArgs

Un gestionnaire d'événements pour l'événement [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) peut fonctionner avec l'objet d'événement [SignEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.aspx) qui offre les propriétés suivantes. 
  
|**Name**|**Description**|
|:-----|:-----|
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignedDataBlock.aspx) <br/> |Obtient l’ensemble des données qui ont créé [l’événement Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) . |
|[SignatureWizard](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignatureWizard.aspx) <br/> |Obtient ou définit l'affichage de la boîte de dialogue **Signatures numériques**. |
   
> [!NOTE]
> [!REMARQUE] Dans le modèle objet de code managé [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) livré avec InfoPath 2003, l'objet d'événement [SignEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.aspx) pour l'événement [OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2.OnSign.aspx) fournit une propriété **XDocument** qui permet d'accéder à l'objet **XDocument** du formulaire associé à l'événement. Ceci n'est pas nécessaire avec les modèles de formulaires créés avec InfoPath Forms Services ou InfoPath à l'aide du modèle objet [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) car les membres du modèle objet de la classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) sont accessibles dans le code du formulaire à l'aide du mot clé **this** (C#) ou **Me** (Visual Basic). Par exemple, pour accéder à la propriété [Signed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx) de la classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) afin de déterminer si un formulaire est signé, vous pouvez taper  `this.Signed` ou  `Me.Signed.`
  
### <a name="collections-and-objects"></a>Collections et objets

Le modèle objet des signatures numériques fournit les collections suivantes.
  
|**Name**|**Description**|
|:-----|:-----|
|[SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) <br/> |Collection des objets [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) dans le modèle de formulaire tel que défini au moment de la conception en mode Création d’InfoPath. La collection [SignedDataBlockCollection implémente](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) des propriétés qui peuvent être utilisées pour accéder aux objets [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) associés à un formulaire. [L’objet SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) associé à un formulaire est accessible via la propriété [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx) de la [classe XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx). |
|[SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) <br/> |Contient une collection [d’objets Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) pour [chaque objet SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) du formulaire. La [classe SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) implémente des propriétés et une méthode qui peuvent être utilisées pour accéder aux objets [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) associés d’un formulaire et pour créer une signature. [L’objet SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) associé à [un SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) est accessible à l’aide de la [propriété Signatures](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Signatures.aspx). Lorsque vous utilisez la méthode [CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) de la [classe SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) , n’oubliez pas que la signature n’est pas écrite tant que la méthode [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) n’est pas appelée sur [l’objet Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) . Ces méthodes peuvent être appelées uniquement depuis le gestionnaire d'événements **Sign** d'un modèle de formulaire entièrement fiable. |
   
Le modèle objet des signatures numériques fournit les objets suivants.
  
|**Name**|**Description**|
|:-----|:-----|
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |Représente un ensemble de données à signer dans un formulaire. L'objet [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) fournit une méthode et un certain nombre de propriétés qui peuvent être utilisées pour interagir par programme avec un ensemble de données à signer. |
|[Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |Représente une signature numérique qui a été ajoutée à un formulaire ou à un ensemble de données signables dans un formulaire. L’objet [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) implémente des propriétés qui peuvent être utilisées pour récupérer des informations sur la signature numérique et la méthode [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) pour écrire le bloc de signature numérique XML et calculer sa valeur de hachage de chiffrement. |
|[Certificat](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.aspx) <br/> |Représente le certificat numérique X.509 utilisé pour créer la signature. |
   
## <a name="working-with-digital-signatures-programmatically"></a>Utilisation de signatures numériques par programme

Le modèle objet de l'espace de noms [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) fournit les membres qui permettent d'interagir avec les signatures numériques par programmation. Plus spécifiquement, les formulaires entièrement fiables peuvent ajouter des informations personnalisées au bloc de signature avant sa validation, selon la séquence suivante : 
  
1. L'utilisateur choisit d'ajouter une signature numérique à un formulaire.
    
2. La boîte de dialogue **Signatures numériques** s'affiche, l'utilisateur clique sur **Ajouter**, puis il sélectionne les données à signer.
    
3. L'événement [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) des données sélectionnées, représentées par l'objet [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) , est déclenché et la méthode [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) de l'objet [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) et la méthode [CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) de la collection [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) s'exécutent. 
    
4. Les actions personnalisées facultatives sont exécutées.
    
5. La méthode [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) de l'objet [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) s'exécute. 
    
6. La boîte de dialogue **Signature** s'affiche pour vous permettre d'entrer un nom (ou de sélectionner une image de signature), de sélectionner un certificat de signature et d'entrer des commentaires. 
    
7. Lorsque vous cliquez sur le bouton **Signer**, la signature est ajoutée à la collection de signatures du formulaire et les informations de non-répudiation sont capturées et enregistrées avec la signature (qui peut être affichée plus tard en cliquant sur **Afficher le formulaire signé** dans la boîte de dialogue **Signatures numériques**, puis en cliquant sur **Voir les informations complémentaires rassemblées sur les signatures**).
    
L'exemple suivant appelle la méthode [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) lorsque l'utilisateur signe les données sélectionnées et contre-signe la signature avec une valeur d'horodatage récupérée à partir d'un service d'horodatage approuvé. 
  
```cs
public void FormEvents_Sign(object sender, SignEventArgs e)
{
   // Add a new Signature object to the SignedDataBlockCollection.
   Signature thisSignature = 
      e.SignedDataBlock.Signatures.CreateSignature();
   // Write the XML digital signature block and compute hash
   // for signed data.
   thisSignature.Sign();
   // Countersign the signature with a trusted timestamp.
   // Get the XML node storing the signature block.
   XPathNavigator oNodeSig = thisSignature.SignatureBlockXmlNode;
   XPathNavigator oNodeSigValue = 
      oNodeSig.SelectSingleNode(
      ".//*[local-name(.)='signatureValue']");
   // Get timestamp from a trusted timestamp service (fictitious).
   MyTrustedTimeStampService s = new MyTrustedTimeStampService();
   string strVerifiedTimeStamp = s.AddTimeStamp(oNodeSigValue.Value);
   // Add the value returned from the timestamp service to the 
   // unsigned part of the signature block.
   XPathNavigator oNodeObj = 
      oNodeSig.SelectSingleNode(".//*[local-name(.)='Object']");
   XPathNavigator oNode = oNodeObj.Clone();
   oNode.SetValue(strVerifiedTimeStamp);
   oNodeObj.MoveToParent();
   oNodeObj.AppendChild(oNode);
   e.SignatureWizard = false;
}
```

```vb
Public Sub FormEvents_Sign(ByVal sender As Object, _
   ByVal e As SignEventArgs)
   ' Add a new Signature object to the SignedDataBlockCollection.
   Dim thisSignature As Signature = 
      e.SignedDataBlock.Signatures.CreateSignature
   ' Write the XML digital signature block and compute hash
   ' for signed data.
   thisSignature.Sign()
   ' Countersign the signature with a trusted timestamp.
   ' Get the XML node storing the signature block
   Dim oNodeSig As XPathNavigator  = _
      thisSignature.SignatureBlockXmlNode
   Dim oNodeSigValue As XPathNavigator  = _
      oNodeSig.SelectSingleNode(_
      ".//*[local-name(.)='signatureValue']")
   ' Get timestamp from a trusted timestamp service (fictitious).
   Dim s As MyTrustedTimeStampService = New MyTrustedTimeStampService()
   Dim strVerifiedTimeStamp As String  = _
      s.AddTimeStamp(oNodeSigValue.Value)
   ' Add the value returned from the timestamp service to the 
   ' unsigned part of the signature block.
   Dim oNodeObj As XPathNavigator  = 
      oNodeSig.SelectSingleNode(".//*[local-name(.)='Object']")
   Dim oNode As XPathNavigator  = oNodeObj.Clone()
   oNode.SetValue(strVerifiedTimeStamp)
   oNodeObj.MoveToParent()
   oNodeObj.AppendChild(oNode)
   e.SignatureWizard = False
```


