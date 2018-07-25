---
title: Nouveautés pour les développeurs InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- what's new [infopath 2007],developer features [InfoPath 2007],InfoPath 2007, what's new,new features [InfoPath 2007]
localization_priority: Normal
ms.assetid: d0ad3111-bd41-4f35-8a34-62c17f20fc19
description: InfoPath est conçu pour faciliter la création d'applications basées sur des formulaires riches sur la plateforme Microsoft SharePoint Server. Microsoft InfoPath 2013, Microsoft SharePoint Server 2013 et InfoPath Forms Services offrent de nombreuses fonctionnalités aux développeurs. InfoPath Forms Services, qui est disponible dans SharePoint Server 2013, vous permet de déployer un modèle de formulaire InfoPath vers un SharePoint Server, de manière à ce que les utilisateurs sans le client riche InfoPath puissent ouvrir et remplir les formulaires InfoPath dans un navigateur web.
ms.openlocfilehash: a11c6b4018e60a470197ecd7ffdf3b79a13658b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782469"
---
# <a name="whats-new-for-infopath-developers"></a>Nouveautés pour les développeurs InfoPath

InfoPath est conçu pour faciliter la création d'applications basées sur des formulaires riches sur la plateforme Microsoft SharePoint Server. Microsoft InfoPath 2013, Microsoft SharePoint Server 2013 et InfoPath Forms Services offrent de nombreuses fonctionnalités aux développeurs. InfoPath Forms Services, qui est disponible dans SharePoint Server 2013, vous permet de déployer un modèle de formulaire InfoPath vers un SharePoint Server, de manière à ce que les utilisateurs sans le client riche InfoPath puissent ouvrir et remplir les formulaires InfoPath dans un navigateur web.
  
Les modèles de formulaire créés avec InfoPath 2013 prennent toujours en charge la logique métier écrite pour les classes et les membres de l'espace de noms **Microsoft.Office.InfoPath**, qui fonctionne de la même manière pour un formulaire ouvert dans InfoPath Filler et pour un formulaire ouvert dans un navigateur web. En utilisant la logique métier écrite pour ce modèle objet managé et en utilisant les fonctionnalités de vérification de la conception dans InfoPath Designer, vous pouvez créer un modèle de formulaire unique que vous pouvez déployer sur une bibliothèque de document configurée de manière appropriée sur SharePoint Server 2013, qui sera exécutée dans InfoPath Filler et dans un navigateur web. 
  
## <a name="new-features-and-improvements"></a>Améliorations et nouvelles fonctionnalités

Les sections suivantes décrivent brièvement les fonctionnalités et améliorations susceptibles d'intéresser les développeurs InfoPath :
  
- Nouvelle méthode pour écrire et modifier du code
    
- Solutions SharePoint en bac à sable
    
- Publier des formulaires en un seul clic
    
- Améliorer les formulaires de liste SharePoint
    
- Héberger des formulaires sur des pages de portail à l'aide du composant WebPart Formulaire InfoPath
    
- Formulaires Web riches en fonctionnalités
    
- Formulaires de navigateur compatibles avec les normes
    
- Fournir une intégrité et une sécurité des informations renforcées avec les signatures numériques
    
- Nouveaux contrôles
    
## <a name="new-way-to-write-and-edit-code"></a>Nouvelle méthode pour écrire et modifier du code

L'IDE Microsoft Visual Studio Tools for Applications qui était intégré à InfoPath 2010 a été supprimé dans InfoPath 2013. Pour écrire ou modifier du code de formulaire dans InfoPath 2013, Visual Studio 2012 et le complément [Microsoft Visual Studio Tools for Applications 2012](http://www.microsoft.com/en-us/download/details.aspx?id=38807) doivent être installés. L'expérience de programmation à proprement parler n'a pas changé de manière fondamentale, mais vous pouvez désormais utiliser l'expérience de développement Visual Studio complète lorsque vous écrivez du code managé pour vos formulaires InfoPath. 
  
Les sections suivantes décrivent les fonctionnalités qui ont d'abord été ajoutées dans InfoPath 2010 et SharePoint Server 2010 et qui restent une valeur ajoutée pour les développeurs utilisant InfoPath 2013 et SharePoint Server 2013.
  
## <a name="sharepoint-server-sandboxed-solutions"></a>Solutions SharePoint Server en bac à sable

Avec InfoPath, il n'a jamais été aussi facile de déployer des formulaires avec du code dans SharePoint Server 2013. Dans Office InfoPath 2007, tous les formulaires comportant du code devaient être approuvés et téléchargés par un administrateur de batterie de serveurs SharePoint. Grâce à la prise en charge de solutions bac à sable dans SharePoint Server 2013, les concepteurs de formulaires disposant des autorisations d'administration d'une collection de sites peuvent désormais publier la plupart des formulaires avec du code directement sur leurs sites SharePoint. Un paramètre de quota de ressources sur le serveur limite l'utilisation excessive des ressources. L'administrateur de collection de sites reste dans le contrôle et prend des décisions d'approbation en ce qui concerne la solution. L'administrateur de batterie de serveurs peut ne pas intervenir. Pour plus d'informations sur la publication de modèles de formulaires InfoPath en tant que solutions bac à sable, voir [Publication de formulaires avec code](publishing-forms-with-code.md).
  
## <a name="publish-forms-with-one-click"></a>Publier des formulaires en un seul clic

InfoPath est conçu pour faciliter encore plus la publication de mises à jour dans vos formulaires. Après la première publication d'un modèle de formulaire, plutôt que de cliquer dans plusieurs boîtes de dialogue, vous pouvez effectuer cette tâche en un seul clic sur le nouveau bouton **Publication rapide**, disponible sur la **Barre d'outils Accès rapide**, et dans le nouveau Microsoft Office Backstage, disponible en cliquant sur l'onglet **Fichier**. 
  
## <a name="enhance-sharepoint-list-forms"></a>Améliorer les formulaires de liste SharePoint

Avec InfoPath, vous pouvez désormais étendre et améliorer les formulaires utilisés pour créer, modifier et afficher les éléments dans une liste SharePoint. À l'ouverture d'une liste, cliquez sur l'onglet **Liste** sous **Outils de liste**, puis en cliquant sur **Personnaliser un formulaire**, vous pouvez générer automatiquement un formulaire InfoPath qui ressemble au formulaire de liste SharePoint prêt à l'emploi par défaut. Vous pouvez ensuite personnaliser et améliorer ce formulaire en modifiant la mise en page, en créant des vues supplémentaires et en ajoutant des règles et des validations de données dans InfoPath. Lorsque vous avez terminé de modifier votre formulaire de liste amélioré, vous pouvez le publier sur SharePoint à l'aide de la nouvelle fonctionnalité de publication en un clic dans InfoPath.
  
## <a name="host-forms-on-portal-pages-using-the-infopath-form-web-part"></a>Héberger des formulaires sur des pages de portail à l'aide du composant WebPart Formulaire InfoPath

Dans SharePoint Server 2013, il est plus facile que jamais d’héberger vos formulaires sur des pages Web en utilisant le nouveau **composant WebPart Formulaire InfoPath**. Dans Microsoft Office SharePoint Server 2007, les utilisateurs qui souhaitent héberger leurs formulaires InfoPath sur les pages Web doivent écrire le code dans Visual Studio. À présent et sans écrire une seule ligne de code, vous pouvez ajouter le **composant WebPart Formulaire InfoPath** à une page WebPart et le faire pointer vers votre formulaire publié. Vous pouvez utiliser le **composant WebPart Formulaire InfoPath** pour héberger un formulaire de navigateur InfoPath qui est publié dans une bibliothèque de liste ou de formulaires SharePoint. Vous pouvez également vous connecter aux autres composants WebPart sur la page pour envoyer ou recevoir des données. Pour plus d’informations sur l’utilisation du **composant WebPart Formulaire InfoPath**, consultez [Manipuler le composant WebPart Formulaire InfoPath](http://msdn.microsoft.com/library/bb87e126-1a07-45aa-af36-b294df3a2576%28Office.15%29.aspx) dans le SDK SharePoint 2010. 
  
## <a name="richer-web-forms"></a>Formulaires Web riches en fonctionnalités

L'écart de fonctionnalité entre les formulaires clients et les formulaires de navigateur a été réduit ; l'expérience du remplissage des formulaires est ainsi plus cohérente pour l'ensemble des utilisateurs. Les contrôles et les fonctions maintenant pris en charge dans les formulaires de navigateur sont notamment :
  
- Listes à puces, numérotées et simples
    
- Zones de liste à sélection multiple
    
- Zones de liste déroulante
    
- Boutons images
    
- Possibilités de lien hypertexte
    
- Groupe et section de choix 
    
- Contrôles de date et d'heure
    
- Sélecteurs de personnes/groupes
    
- Fonctionnalité de filtrage
    
## <a name="standards-compliant-browser-forms"></a>Formulaires de navigateur compatibles avec les normes

Les formulaires de navigateur InfoPath sont désormais compatibles avec les normes pour l'accessibilité au contenu web (WCAG) 2.0 AA, qui permettent aux concepteurs de formulaires de créer des formulaires accessibles aux utilisateurs handicapés.
  
## <a name="provide-enhanced-information-security-and-integrity-with-digital-signatures"></a>Fournir une intégrité et une sécurité des informations renforcées avec les signatures numériques

InfoPath prend en charge le contenu CNG (Cryptography Next Generation) signé numériquement. Pour vous aider à garantir l'intégrité des informations contenues dans vos formulaires, le client InfoPath et SharePoint Server 2013 fournissent les contrôles nécessaires pour activer des scénarios uniques, cosignés et contresignés pour l'intégralité ou quelques sections du formulaire. Les formulaires peuvent être signés dans Internet Explorer à l'aide du contrôle de ligne de signature ActiveX. Les formulaires signés peuvent être affichés dans tous les navigateurs pris en charge par SharePoint Server 2013.
  
## <a name="new-controls"></a>Nouveaux contrôles

InfoPath fournit un jeu de contrôles plus riche, que vous pouvez ajouter à vos formulaires. La liste suivante décrit brièvement certains des nouveaux contrôles :
  
- **Bouton Image**: au lieu d'un rectangle gris, utilisez une image comme bouton dans votre formulaire. 
    
- **Lien hypertexte**: permet aux utilisateurs d'entrer leurs propres liens hypertexte lors du remplissage des formulaires. 
    
- **Sélecteur de personnes/groupes**: permet aux utilisateurs de vérifier et d'interroger les groupes et noms de compte lors du remplissage des formulaires. 
    
- **Sélecteur d'entités**: permet aux utilisateurs de sélectionner des valeurs dans des listes externes sur un serveur qui exécute des formulaires SharePoint Server 2013. 
    
- **Ligne de signature**: fournit à l'utilisateur une ligne de signature ou une image de tampon, comme un sceau inkan ou hanko, lors de la signature numérique de formulaires. 
    
## <a name="see-also"></a>Voir aussi



[Développement de modèles de formulaire InfoPath avec code](developing-infopath-form-templates-with-code.md)
  
[Développement de modèles de formulaires à l’aide du modèle objet InfoPath 2003](developing-form-templates-using-the-infopath-2003-object-model.md)

