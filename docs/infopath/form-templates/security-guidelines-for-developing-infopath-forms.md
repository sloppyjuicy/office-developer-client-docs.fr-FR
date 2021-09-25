---
title: Consignes de sécurité pour développer des formulaires InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 4690028e-20ac-297b-4651-801f5159c747
description: Avant de lire cette rubrique, consultez Autres concepts de sécurité pour les formulaires InfoPath pour une présentation générale du modèle de sécurité InfoPath.
ms.openlocfilehash: 4e1d42fcc47d58b540bff752e183830dcd4f022d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557399"
---
# <a name="security-guidelines-for-developing-infopath-forms"></a>Consignes de sécurité pour développer des formulaires InfoPath

Avant de lire cette rubrique, consultez [Autres concepts de sécurité pour les formulaires InfoPath](additional-infopath-form-security-concepts.md) pour une présentation générale du modèle de sécurité InfoPath. 
  
## <a name="security-issues-for-users-of-infopath-forms"></a>Problèmes de sécurité pour les utilisateurs de formulaires InfoPath

Les principales préoccupations quant à la sécurité pour les utilisateurs de Microsoft InfoPath sont similaires à celles qui concernent les applications Web s'exécutant dans Internet Explorer. Notez cependant que le niveau de sécurité fourni pour un formulaire dépend seulement de l'endroit où se trouve le modèle du formulaire, et non pas de l'endroit où les utilisateurs stockent ou ouvrent les documents XML résultants qu'ils créent. Les utilisateurs peuvent déterminer l'emplacement du modèle de formulaire avec lequel ils travaillent en consultant la barre d'état d'InfoPath.
  
InfoPath aide à protéger les utilisateurs contre les menaces potentielles suivantes provenant de modèles de formulaires créés avec des intentions malveillantes :
  
- La possibilité de divulgation d'informations sensibles de l'ordinateur local ou de sources de données distantes.
    
- L'utilisation malveillante de contrôles ActiveX.
    
- L’utilisation malveillante de propriétés et de méthodes du modèle objet InfoPath.
    
## <a name="disclosure-of-sensitive-information"></a>Divulgation d’informations sensibles

Le scénario le plus courant de divulgation d'informations sensibles peut se produire si un créateur de formulaires malveillant crée un formulaire qui utilise les informations d'identification de l'utilisateur actuel pour accéder à une source de données sur un domaine autre que celui sur lequel le formulaire lui-même a été déployé. Par exemple, un utilisateur malveillant peut envoyer un formulaire par courrier électronique ou à l’aide d’une URL vers un formulaire sur un partage privé ou un serveur Web. Le formulaire peut contenir un script qui effectue une demande d'accès aux données à l'aide des informations d'identification de l'utilisateur actuel, pour récupérer des données d'une source de données dans un autre domaine auquel sans cela l'utilisateur malveillant n'a pas accès, telle qu'une base de données des salaires ou d'autres informations sensibles. Cette classe de scénarios de risques de sécurité est connue sous le nom d'accès aux données d'autres domaines.
  
Le modèle de sécurité Internet Explorer sur lequel est basé InfoPath fournit un paramètre nommé **Accès aux sources de données sur plusieurs domaines**, qui désactive par défaut l'accès à d'autres domaines pour les formulaires InfoPath qui se trouvent dans les zones de sécurité **Internet** et **Sites sensibles**. Ce paramètre demande aussi à l'utilisateur d'autoriser ou d'interdire l'accès à d'autres domaines pour les formulaires InfoPath qui se trouvent dans la zone de sécurité **Intranet local**, et il permet l'accès à d'autres domaines pour les formulaires InfoPath qui se trouvent dans les zones **Sites de confiance** ou **Ordinateur local**. 
  
## <a name="malicious-use-of-activex-controls"></a>Utilisation malveillante de contrôles ActiveX

Le scénario principal d'utilisation malveillante de contrôles ActiveX se produit lorsqu'un créateur de formulaires malveillant écrit du code pour un contrôle ActiveX qui accède au système de fichiers pour extraire des fichiers personnels et des listes de mots de passe, pour supprimer des fichiers ou pour désactiver le système de l'utilisateur. Un formulaire InfoPath peut exécuter du code pour des contrôles ActiveX seulement pour une logique métier ou pour un script s'exécutant dans un volet Office. InfoPath interdit aux scripts dans des vues InfoPath d'exécuter des contrôles ActiveX.
  
Le modèle de sécurité Internet Explorer sur lequel est basé InfoPath fournit un paramètre nommé **Contrôles d'initialisation et de script ActiveX non marqués comme sécurisés**. Ce paramètre désactive par défaut l'initialisation et l'exécution des scripts de contrôles ActiveX marqués comme étant non sécurisés pour les formulaires InfoPath qui se trouvent dans les zones de sécurité **Intranet local**, **Internet** et **Sites sensibles**. Il demande à l'utilisateur d'autoriser ou d'interdire l'exécution des scripts de contrôles ActiveX marqués comme étant non sécurisés pour les formulaires InfoPath qui se trouvent dans les zones de sécurité **Sites de confiance** ou **Ordinateur local**, et il permet l'exécution des scripts de contrôles ActiveX marqués comme étant non sécurisés pour les formulaires InfoPath qui sont entièrement fiables. 
  
En outre, vous ne pouvez pas insérer un contrôle ActiveX qui est marqué comme étant non sécurisé pour l'initialisation et l'exécution de scripts dans le volet Office en mode Création, quelle que soit la zone de sécurité où vous vous trouvez ou le niveau de confiance du formulaire.
  
## <a name="malicious-use-of-infopath-object-model-code"></a>Utilisation malveillante de code du modèle objet InfoPath

De la même façon, des méthodes et des propriétés InfoPath appelées depuis du code peuvent présenter différents niveaux de risques. Par exemple, la méthode [SaveAs(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx) de la classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) peut être utilisée pour écrire des données n'importe où dans le système de fichiers. Pour aider à la protection contre l'utilisation malveillante de ces membres du modèle objet, le modèle objet InfoPath implémente trois niveaux de sécurité qui déterminent comment et où un membre particulier du modèle objet peut être utilisé. Pour plus d’informations sur cette fonctionnalité, voir à propos du modèle de sécurité pour les [modèles de formulaires avec code.](about-the-security-model-for-form-templates-with-code.md)
  
## <a name="best-practices-for-developers-of-infopath-forms"></a>Meilleures pratiques pour les développeurs de formulaires InfoPath

Les développeurs créant des formulaires InfoPath doivent savoir comment implémenter les meilleures pratiques de sécurité suivantes :
  
- Comment reconnaître des problèmes de sécurité potentiels dans le fichier XML associé à un formulaire.
    
- Comment éviter de présenter des messages d'erreur confus ou ennuyeux aux utilisateurs de formulaires.
    
- Comment signer les fichiers CAB des contrôles ActiveX.
    
- Comment signer des modèles de formulaire envoyés en tant que pièces jointes à un message électronique.
    
## <a name="best-practices-for-xml-data-associated-with-a-form"></a>Meilleures pratiques pour les données XML associées à un formulaire

Notez que les formulaires InfoPath peuvent être alimentés en données XML depuis n'importe quelle source, y compris celles que l'utilisateur ne contrôle pas nécessairement ou auxquelles il ne fait pas nécessairement confiance. Par exemple, InfoPath peut obtenir des données XML à partir d’un lien vers une page Web ou d’une pièce jointe XML envoyée à l’utilisateur dans un message électronique. Pour réduire ces risques, tenez compte des meilleures pratiques suivantes :
  
- Ne passez pas des données non approuvées qui sont lues depuis le code XML à la fonction Microsoft JScript **eval()** ou la propriété **innerHTML** du volet Office. Ces deux appels peuvent être utilisés pour exécuter des scripts malveillants. Dans un volet Office, utilisez à la place la propriété **innerText**. Notez que les vues InfoPath ne peuvent pas exécuter de scripts. 
    
- Les données envoyées à une base de données depuis un fichier XML peuvent présenter des risques de sécurité pour la base de données si elles ne sont pas validées avant d'être envoyées.
    
Les données qui ne sont pas validées avant d'être envoyées à une source de données peuvent endommager l'intégrité des données de la source de données ou, dans les cas plus extrêmes, présenter le risque potentiel de saturations de la mémoire tampon. Il est également possible de provoquer l'injection de scripts ou de code SQL si vous essayez d'utiliser des données non approuvées directement sur votre serveur.
  
## <a name="best-practices-to-avoid-presenting-confusing-error-messages"></a>Meilleures pratiques pour éviter la présentation de messages d’erreur confus

 **Déployer des formulaires et leurs sources de données sur le même domaine**
  
Le risque de sécurité d'accès aux données d'autres domaines n'est pas clairement compris par la plupart des utilisateurs. Le déploiement de formulaires qui avertissent et invitent continuellement les utilisateurs quant à l'autorisation d'accès aux données d'autres domaines a comme effet d'inciter beaucoup d'utilisateurs à approuver toutes les demandes d'accès à d'autres domaines ou à ajouter le domaine de provenance à leur liste **Sites de confiance** sans considérer sérieusement les risques de sécurité. Pour éviter cette situation, déployez les formulaires InfoPath sur le même serveur que les sources de données dont ils dépendent. 
  
 **Éviter d'utiliser des contrôles ActiveX qui ne sont pas marqués comme étant sécurisés pour les scripts**
  
Les contrôles ActiveX peuvent potentiellement exposer des propriétés et des méthodes qui peuvent être utilisées pour compromettre le système d'un utilisateur, telles que des méthodes pour accéder au système de fichiers d'un ordinateur. Lorsque c'est possible, vous ne devez utiliser que des contrôles ActiveX marqués comme étant sécurisés pour les scripts. Il s'agit de contrôles qui ont été testés pour vérifier qu'ils n'endommagent pas le système d'un utilisateur ni ne compromettent la sécurité de l'utilisateur, quelle que soit la façon dont les méthodes et les propriétés du contrôle sont manipulées par un script d'une page Web. De la même façon, lors de la création de contrôles ActiveX à utiliser avec InfoPath, inspectez le code et testez le contrôle ActiveX rigoureusement avant de le marquer comme étant sécurisé pour les scripts.
  
InfoPath utilise un modèle de sécurité qui est basé sur les zones de sécurité d'Internet Explorer. Par conséquent, un formulaire InfoPath utilise les mêmes autorisations qu'Internet Explorer, qui permet par défaut les appels de scripts à des contrôles ActiveX marqués comme étant sécurisés pour les scripts, sans en demander l'autorisation aux utilisateurs.
  
## <a name="best-practices-for-managing-the-cab-files-of-activex-controls"></a>Meilleures pratiques pour la gestion des fichiers CAB des contrôles ActiveX

Les contrôles ActiveX peuvent être hébergés dans des modèles de formulaire conçus pour l'éditeur d'InfoPath. Les fichiers CAB pour ces contrôles qui ne sont pas déjà présents sur l'ordinateur de l'utilisateur doivent être inclus dans le fichier du modèle de formulaire (.xsn). Les fichiers CAB inclus dans les modèles de formulaire doivent être signés numériquement pour pouvoir être installés. InfoPath n'installe pas un fichier CAB qui n'est pas signé, quel que soit le niveau de confiance ou la zone de sécurité.
  
Pour faire en sorte que la signature numérique sur le fichier CAB puisse être vérifiée, le fichier doit être signé avec un certificat qui a une chaîne d'approbation conduisant à une racine de certificat déjà approuvée. Sinon, la signature ne peut pas être authentifiée, la vérification de la signature échoue et le fichier CAB n'est pas installé.
  
## <a name="best-practices-for-form-templates-sent-as-an-attachment-to-an-email-message"></a>Meilleures pratiques pour les modèles de formulaire envoyés en tant que pièces jointes à un message électronique

InfoPath prend en charge le déploiement de modèles de formulaire en tant que pièces jointes à un message électronique et le déplacement de modèles de formulaire d’un emplacement à un autre. Il est de bonne pratique en matière de sécurité de signer numériquement un modèle de formulaire que vous concevez et que vous envisagez de déployer en tant que pièce jointe à un message électronique. Une signature numérique sur un modèle de formulaire déployé par message électronique garantit non seulement l’authenticité du modèle. Il présente également l’avantage de permettre la mise à jour automatique du modèle de formulaire.
  
Le modèle de formulaire doit être signé avec un certificat qui a une chaîne d'approbation conduisant à une racine de certificat déjà approuvée. S'il n'est pas signé avec un tel certificat, la vérification de la signature échoue car elle ne peut pas être authentifiée.
  
> [!NOTE]
> [!REMARQUE] Si un modèle de formulaire signé demande un accès au domaine ou un accès restreint, InfoPath ne vérifie pas la signature, sauf pour déterminer si InfoPath peut mettre à jour le modèle automatiquement. 
  
Vous trouverez plus d’informations sur le déploiement du courrier électronique dans les niveaux de sécurité, le déploiement de messagerie électronique [et les modèles de formulaire distants.](security-levels-email-deployment-and-remote-form-templates.md)
  

