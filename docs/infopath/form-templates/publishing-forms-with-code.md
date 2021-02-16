---
title: Publication de formulaires avec code
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: caafab24-6413-4731-813d-cba3ae9ea97e
description: Tout administrateur de collection de sites peut publier des formulaires avec du code directement à partir de l’Assistant Publication InfoPath Designer vers une bibliothèque de formulaires sur SharePoint. Le code est exécuté dans un environnement « bac à sable » (sandbox) afin d'éviter que du code malveillant puisse nuire au serveur. On désigne cela par publication d'une solution en bac à sable (sandbox) ou publication sur l'infrastructure sandbox SharePoint.
ms.openlocfilehash: f8f8a48ea6810b5331198f6ddc112b3bd38ab886
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428325"
---
# <a name="publishing-forms-with-code"></a>Publication de formulaires avec code

Tout administrateur de collection de sites peut publier des formulaires avec du code directement à partir de l’Assistant Publication InfoPath Designer vers une bibliothèque de formulaires sur SharePoint. Le code est exécuté dans un environnement « bac à sable » (sandbox) afin d'éviter que du code malveillant puisse nuire au serveur. On désigne cela par publication d'une solution en bac à sable (sandbox) ou publication sur l'infrastructure sandbox SharePoint.
  
InfoPath 2010 et SharePoint Server 2010 permettent également la prise en charge des solutions déployées par l’administrateur. Un concepteur de formulaires publie des formulaires avec du code dans un magasin local, qui sont ensuite révisés et chargés par un administrateur de batterie SharePoint. La confiance totale est octroyée à ce code, qui peut incorporer des fonctionnalités nécessitant des privilèges élevés tels que E/S fichier.
  
## <a name="comparing-sandboxed-and-administrator-approved-solutions"></a>Comparaison entre les solutions en bac à sable (sandbox) et celles approuvées par l’administrateur

Le tableau suivant récapitule les différences de la publication pour ces deux types de solutions.  
  
||**Solutions bac à sable**|**Solutions approuvées par l’administrateur**|
|:-----|:-----|:-----|
|**Autorisations requises** <br/> |Publiables par tout administrateur de collection de sites.  <br/> |Déployables par un administrateur de batterie.  <br/> |
|**Publishing** <br/> |Peut être publié directement à partir d’InfoPath.  <br/> |Déployables en utilisant l’Administration centrale ou l’outil de ligne de commande stsadm.  <br/> |
|**Protection** <br/> |Le code est exécuté dans un environnement « bac à sable » (sandbox) afin de protéger le serveur contre du code malveillant.  <br/> |Le code peut s’exécuter avec autorisation totale et accéder à toutes les ressources sur le serveur.  <br/> |
|**Utilisation recommandée** <br/> |Formulaires nécessitant une petite quantité de code seulement.  <br/> |Formulaires contenant de nombreuses lignes de code.  <br/> |
   
### <a name="publishing-form-templates-as-sandboxed-solutions"></a>Publication de modèles de formulaire en tant que solutions en bac à sable (sandbox)

La publication d'un formulaire avec du code en tant que solution bac à sable n'est pas différente de celle de tout autre formulaire dans une bibliothèque de documents. Utilisez simplement l'assistant de publication comme d'habitude et votre formulaire sera chargé sur le serveur et fonctionnera dans le bac à sable.
  
Notez que le déploiement de votre formulaire en tant que solution bac à sable comporte certaines restrictions :
  
- Ce doit être un formulaire InfoPath.
    
- Il doit utiliser C# ou Visual Basic comme langage de programmation.
    
- Impossible d’envoyer des données aux connexions de données par courrier électronique.
    
- Il ne peut pas avoir des propriétés promues pour des connexions partie-à-partie.
    
- Il ne peut pas comporter des connexions de données ni des contrôles de métadonnées gérées.
    
Pour permettre aux administrateurs de collection de sites d'utiliser solutions bac à sable sur Microsoft SharePoint Server 2010 ou sur un serveur qui exécute Microsoft SharePoint Foundation 2010, l'administrateur de batterie doit démarrer le service de code utilisateur Windows SharePoint.
  
### <a name="to-start-the-windows-sharepoint-user-code-service"></a>Pour démarrer le service de code utilisateur Windows SharePoint

1. Ouvrez l’Administration centrale.
    
2. Sous **Services système**, cliquez sur **Gérer les services sur le serveur**.
    
3. Démarrez le **Service de code utilisateur Microsoft SharePoint Foundation**.
    
### <a name="to-publish-a-sandboxed-solution"></a>Pour publier une solution en bac à sable (sandbox)

1. Ouvrez le modèle de formulaire dans le concepteur InfoPath.
    
2. Cliquez sur l'onglet **Fichier**, puis cliquez sur **SharePoint Server** sur l'onglet **Publier** dans Backstage. 
    
3. Entrez l'URL du site SharePoint sur lequel publier, puis cliquez sur **Suivant**. 
    
    > [!IMPORTANT]
    > [!IMPORTANTE] Vous devez être administrateur de collection de sites sur ce site pour publier ce modèle de formulaire en tant que solution bac à sable. 
  
4. Sélectionnez **Bibliothèque de formulaires**, puis cliquez sur **Suivant**.
    
5. Sélectionnez **Créer une bibliothèque de formulaires**, puis cliquez sur **Suivant**.
    
6. Entrez le nom et la description de votre bibliothèque de formulaires, puis cliquez sur **Suivant**.
    
7. Cliquez sur **Publier**.
    
Pour des exemples de solutions qui illustrent des scénarios appropriés pour la publication de modèles de formulaires en tant que solutions bac à sable, voir [Exemples de solutions en bac à sable (sandbox)](sample-sandboxed-solutions.md).
  
### <a name="publishing-form-templates-as-administrator-deployed-solutions"></a>Publication de modèles de formulaires en tant que solutions déployées par un administrateur

La publication de votre formulaire en tant que modèle approuvé par l’administrateur est recommandée si votre formulaire comporte de nombreuses connexions de données, s’il nécessite la confiance totale, ou si votre modèle doit être défini à l’échelle de la batterie.
  
Pour un administrateur de batterie, plusieurs étapes sont nécessaires pour fournir une solution déployée par un administrateur sur SharePoint. En tant que développeur, vous devez préparer la solution avant de la soumettre à l'administrateur.
  
Tout d’abord, si votre formulaire doit être déployé avec autorisation totale, vous devez définir le niveau de sécurité comme décrit dans la procédure suivante.
  
### <a name="to-set-the-security-level-of-a-form-template-to-full-trust"></a>Pour définir le niveau de sécurité Autorisation totale pour un modèle de formulaire

1. Ouvrez le modèle de formulaire dans le concepteur InfoPath.
    
2. Cliquez sur l'onglet **Fichier**. Sous l'onglet **Informations**, cliquez sur **Options de formulaire**.
    
3. Cliquez sur la catégorie **Sécurité et approbation**, puis désactivez la case à cocher **Déterminer automatiquement le niveau de sécurité**. 
    
4. Sélectionnez **Confiance totale**.
    
Ensuite, publiez le formulaire en suivant la procédure ci-après. Notez qu’elle comporte certaines différences par rapport à la procédure de publication standard.
  
### <a name="to-publish-an-administrator-deployed-solution"></a>Pour publier une solution déployée par un administrateur

1. Dans la première page de l' **Assistant Publication**, spécifiez l'emplacement du site SharePoint Server 2010 ou SharePoint Foundation 2010, puis cliquez sur **Suivant**.
    
2. InfoPath active automatiquement la case à cocher **Modèle de formulaire approuvé par l'administrateur** sur la seconde page de l'assistant. Cliquez sur **Suivant**.
    
3. La troisième page est destinée uniquement aux scénarios déployés par un administrateur. Au lieu de sélectionner un SharePoint Server, publiez le formulaire dans un magasin local. L'administrateur SharePoint chargera le fichier à partir de cet emplacement durant le processus de déploiement.
    
4. Renseignez les pages restantes de l' **Assistant Publication**.
    

