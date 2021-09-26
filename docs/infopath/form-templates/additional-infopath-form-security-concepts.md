---
title: Autres concepts de sécurité pour les formulaires InfoPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 77425a61-bf33-b3d8-442a-caee48e54a48
description: Le modèle de sécurité Microsoft InfoPath repose sur le modèle de sécurité mis en œuvre par Internet Explorer. Le modèle de sécurité Internet Explorer contribue à protéger votre ordinateur contre les opérations risquées en utilisant des zones et des niveaux de sécurité. En collaborant avec le modèle de sécurité Internet Explorer, InfoPath fournit deux types de déploiement de formulaires qui affectent le fonctionnement d'un formulaire InfoPath au sein de ce modèle de sécurité.
ms.openlocfilehash: 7d3e06f279eace2e750904cfd741d7ffeff5ac9e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631369"
---
# <a name="additional-infopath-form-security-concepts"></a>Autres concepts de sécurité pour les formulaires InfoPath

Le modèle de sécurité Microsoft InfoPath repose sur le modèle de sécurité mis en œuvre par Internet Explorer. Le modèle de sécurité Internet Explorer contribue à protéger votre ordinateur contre les opérations risquées en utilisant des zones et des niveaux de sécurité. En collaborant avec le modèle de sécurité Internet Explorer, InfoPath fournit deux types de déploiement de formulaires qui affectent le fonctionnement d'un formulaire InfoPath au sein de ce modèle de sécurité.
  
- **Formulaires de type URL** Cette méthode de déploiement est utilisée par défaut lors de la publication d'un formulaire d'InfoPath sur un serveur Web, une bibliothèque de formulaires SharePoint Foundation ou un partage de fichiers. Ces formulaires sont dits de type URL, car en général l'utilisateur l'ouvre à partir de l'URL où il est publié ; de plus, cette URL est spécifiée dans l'attribut **publishUrl** de l'élément **xDocumentClass** dans le fichier de définition du formulaire (.xsf). Les formulaires de type URL sont considérés comme étant en sandbox, parce qu'ils ont un accès restreint aux ressources système et autres zones pouvant présenter des risques. Un formulaire de type URL a le même niveau d'autorisations qu'une page Web ouverte à partir du même emplacement que le fichier de modèle de formulaire (.xsn).
    
- **Formulaires de type URN** Cette méthode de déploiement concerne les formulaires qui nécessitent un accès aux ressources système et à d'autres ressources externes, tels que des contrôles ActiveX et d'autres composants logiciels. Vous pouvez déployer des formulaires InfoPath entièrement fiables. Ces formulaires sont également connus sous le nom de formulaires de type URN, car au lieu de spécifier l'attribut **publishUrl**, ils spécifient un URN (Uniform Resource Name) dans l'attribut **name** de l'élément **xDocumentClass** du fichier de définition de formulaire (.xsf). Ce type de formulaire peut nécessiter une confiance totale si l'attribut **requireFullTrust** de l'élément **xDocumentClass** a la valeur  `"yes"` dans le fichier de définition de formulaire (.xsf). Les formulaires de type URN doivent être inscrits sur l'ordinateur client par un programme d'installation ou un script. Dans ce cas, le formulaire bénéficie des mêmes autorisations qu'une application qui s'exécute sur l'ordinateur local. 
    
Avec ces deux méthodes de déploiement de formulaires, chaque méthode et propriété du modèle objet InfoPath dispose d'un niveau de sécurité qui détermine quand cette méthode ou cette propriété peut être appelée à partir du script qui s'exécute depuis le formulaire.
  
## <a name="understanding-infopath-integration-with-the-internet-explorer-security-model"></a>Présentation de l’intégration d’InfoPath avec le modèle de sécurité Internet Explorer

Internet Explorer met en œuvre des zones de sécurité qui vous permettent de contrôler le niveau d'accès accordé à votre ordinateur par les pages Web que vous ouvrez. InfoPath utilise certaines de ces zones pour déterminer le niveau d'accès dont bénéficient les formulaires pour les ressources de votre ordinateur. Par défaut, les formulaires InfoPath s'exécutent dans un emplacement mis en cache qui n'a pas accès aux ressources système essentielles. Les formulaires qui bénéficient d'un accès total aux ressources système sont appelés formulaires entièrement fiables. Ils sont généralement installés et inscrits à l'aide d'un programme d'installation ou d'un script, ou bien ils sont signés numériquement, ce qui leur octroie un niveau d'autorisations supérieur.
  
Les formulaires InfoPath mis en cache sont identifiés par l'URL ou l'URN spécifié dans leur fichier de définition (.xsf). Le type d'identification utilisé et le domaine (emplacement) à partir duquel le modèle de formulaire est ouvert détermine les autorisations de quelle zone de sécurité Internet Explorer le formulaire héritera. Les formulaires identifiés par une URL sont mis en cache sur l'ordinateur de l'utilisateur, ce qui permet de les utiliser en mode hors connexion. Ces formulaires de type URL tiennent leurs autorisations de sécurité et leurs droits d'accès spécifiques, notamment l'accès entre les domaines, des paramètres de sécurité Internet Explorer applicables à l'emplacement original du modèle de formulaire. Les modèles de formulaire stockés sur un serveur Web ou un serveur exécutant SharePoint Foundation s'exécutent dans la zone Intranet locale ou dans la zone Internet, selon le domaine du serveur. Quant aux formulaires installés qui sont identifiés par un URN, ils tiennent leurs autorisations de la zone Ordinateur local, ce qui procure un niveau d'autorisations analogue à celui des fichiers d'application HTML (.hta).
  
Les formulaires entièrement fiables sont identifiés par leur URN et par la définition ou non de l'attribut **requireFullTrust** de l'élément **xDocumentClass** du fichier de définition (.xsf) avec la valeur  `"yes"`. Dans InfoPath, une fois que les formulaires entièrement fiables sont installés, ils apparaissent dans l'onglet **Nouveau** de Microsoft Office Backstage de l'éditeur InfoPath. 
  
Vous trouverez tous les détails sur le fonctionnement des formulaires entièrement fiables et des instructions sur leur création et leur déploiement dans [Présentation des formulaires entièrement fiables](understanding-fully-trusted-forms.md).
  
## <a name="trusting-installed-forms"></a>Approbation des formulaires installés

L'utilisation des formulaires approuvés peut être activée ou désactivée sur des ordinateurs individuels. Lorsqu'un ordinateur est configuré pour approuver les formulaires installés, les utilisateurs peuvent remplir ceux qui nécessitent un accès aux ressources de leur ordinateur.
  
Dans l'éditeur InfoPath, vous configurez un ordinateur pour qu'il approuve les formulaires installés dans Backstage en cliquant sur **Options**, **Centre de gestion de la confidentialité**, **Paramètres du Centre de gestion de la confidentialité**, puis en activant la case à cocher **Autoriser l'exécution des formulaires entièrement fiables sur mon ordinateur** de l'onglet **Éditeurs approuvés** de la boîte de dialogue **Centre de gestion de la confidentialité**. 
  
## <a name="using-security-features-in-infopath"></a>Utilisation des fonctionnalités de sécurité dans InfoPath

Le modèle de sécurité InfoPath permet de protéger les utilisateurs contre les menaces suivantes émanant de modèles créés par des personnes malveillantes :
  
- risque de diffusion d'informations sensibles à partir de votre ordinateur local ou de sources de données distantes ;
    
- utilisation malveillante des contrôles ActiveX ;
    
- utilisation malveillante des propriétés et méthodes du modèle objet InfoPath.
    
## <a name="cross-domain-data-access"></a>Accès aux données d’autres domaines

Un des scénarios risqués pour la sécurité est l'accès aux données d'autres domaines.
  
Le modèle de sécurité Internet Explorer sur lequel repose InfoPath fournit un paramètre appelé **Accès aux sources de données sur plusieurs domaines**. Par défaut, ce paramètre désactive l'accès entre les domaines pour les formulaires InfoPath qui résident dans les zones de sécurité Internet et Sites sensibles. Il demande à l'utilisateur d'autoriser ou de ne pas autoriser l'accès sur plusieurs domaines pour les formulaires InfoPath qui résident dans la zone de sécurité Intranet Local et il autorise l'accès sur plusieurs domaines pour les formulaires InfoPath qui résident dans les zones **Sites approuvés** ou **Ordinateur local**. 
  
## <a name="use-of-the-infopath-html-task-pane"></a>Utilisation du volet des tâches InfoPath HTML

Le volet des tâches InfoPath HTML permet d'afficher les pages Web, tels que des fichiers .htm, .asp et .hta. Les pages référencées à partir des volets des tâches peuvent se trouver à l'intérieur ou à l'extérieur du modèle de formulaire. La seule restriction sur ce qui peut être référencé de l'extérieur du modèle de formulaire, c'est que la page Web doit se trouver dans le même domaine que ce modèle, ou que la zone de sécurité dans laquelle se trouve le modèle accepte les autorisations d'accès sur plusieurs domaines pour charger le volet des tâches.
  
Le volet des tâches ne propose pas de barre d'adresse ni de barre d'état ; l'utilisateur n'a donc aucun moyen de valider l'emplacement de la source pour le volet des tâches ou de s'assurer que cet emplacement est utilise bien un accès sur un canal sécurisé (https). Vous devez donc éviter d'utiliser le volet des tâches pour afficher ou entrer des informations sensibles. Le volet des tâches a été conçu pour afficher des informations d'aide en temps réel et des contrôles pour la navigation entre les vues et les autres éléments d'une solution intégrée. De plus, la logique métier d'un modèle de formulaire et le script du volet des tâches peuvent interagir. Toutefois, cette interaction n'est autorisée que si le modèle de formulaire et le volet des tâches se trouvent dans le même domaine, ce qui permet d'éviter l'échange d'informations entre les domaines.
  
## <a name="cross-domain-data-access-prompts"></a>Messages concernant l’accès aux données d’autres domaines

Si un modèle de formulaire nécessitant un accès aux données d’autres domaines se trouve dans une zone de sécurité définie pour demander cet accès (paramètre par défaut pour la zone Internat Local), l’utilisateur sera invité à indiquer s’il faut autoriser l’accès. Le choix de l’utilisateur reste alors en vigueur tant que le formulaire est ouvert. Si vous devez déployer des modèles de formulaire InfoPath nécessitant un accès aux données sur plusieurs domaines, vous devez déployer ces modèles en tant que formulaires entièrement fiables ou les rendre disponibles sur un serveur situé dans la zone de sécurité Sites approuvés, ce qui évite de demander aux utilisateurs d’autoriser l’accès. Les utilisateurs ne devraient pas être invités à abaisser le niveau de sécurité de la zone Intranet Local pour éviter ces messages.
  
## <a name="forms-without-a-publishurl-attribute"></a>Formulaires sans attribut publishURL

Si InfoPath charge un modèle de formulaire à partir de l'ordinateur local et qu'il a un attribut **publishUrl** vide ou si cet attribut est absent, le formulaire est placé dans une zone de sécurité plus restrictive. Cela permet de réduire la menace de distribution par courrier électronique d’un modèle de formulaire malveillant. Par conséquent, si l’utilisateur enregistre ce modèle de formulaire sur le disque, ce modèle ne pourra pas s’exécuter avec les autorisations d’un formulaire situé dans la zone **Ordinateur local**. 
  
## <a name="unsafe-activex-controls"></a>Contrôles ActiveX non sécurisés

Le scénario le plus courant pour l'utilisation malveillante des contrôles ActiveX peut se produire si un auteur utilise un script avec un contrôle ActiveX fournissant des méthodes pour accéder au système de fichiers afin de récupérer des fichiers personnels et des listes de mots de passe, supprimer des fichiers ou désactiver le système de l'utilisateur. Un formulaire InfoPath ne peut utiliser que des contrôles ActiveX à partir du script du fichier de scripts principal d'un formulaire (script.js) ou d'un script d'un volet de tâches. InfoPath n'accepte pas les scripts des vues InfoPath pour exécuter des contrôles ActiveX.
  
Le modèle de sécurité Internet Explorer sur lequel repose Microsoft InfoPath fournit un paramètre appelé **Contrôles d'initialisation et de script ActiveX non marqués comme sécurisés** qui, par défaut, aboutit aux actions suivantes pour les formulaires InfoPath ou les volets des tâches qui tentent d'initialiser ou d'utiliser dans des scripts des contrôles ActiveX marqués comme non sécurisés pour les scripts. 
  
|**Zone de sécurité/Déploiement**|**Action**|
|:-----|:-----|
|Internet  <br/> |Désactivé  <br/> |
|Intranet local  <br/> |Désactivé  <br/> |
|Sites sensibles  <br/> |Désactivé  <br/> |
|Sites approuvés  <br/> |Invite  <br/> |
|Poste de travail  <br/> |Invite  <br/> |
|Formulaire entièrement fiable  <br/> |Activer  <br/> |
   
## <a name="malicious-use-of-the-infopath-object-model"></a>Utilisation malveillante du modèle objet InfoPath

Comme pour les contrôles ActiveX appelés à partir d'un script, les méthodes et propriétés InfoPath appelées à partir d'un code peuvent présenter différents niveaux de risque. Par exemple, la méthode [SaveAs(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx) de la classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) peut être utilisée pour écrire des données n'importe où dans le système de fichiers. 
  
Pour une meilleure protection contre l'utilisation malveillante des membres du modèle objet InfoPath, ce modèle objet met en œuvre trois niveaux de sécurité qui déterminent comment et où un membre particulier du modèle objet peut être utilisé. Il y a trois niveaux de sécurité dans le modèle objet InfoPath :
  
- **0** Les membres du modèle objet sont accessibles sans restrictions. Ces membres sont sécurisés, de sorte qu'il n'y a pas de restrictions d'accès. 
    
- **2** Les membres du modèle objet sont accessibles uniquement par les formulaires s'exécutant dans le même domaine que le formulaire ouvert, ou par les formulaires qui disposent d'autorisations d'accès aux données sur plusieurs domaines. Les modèles de formulaire qui appellent les méthodes de modèle objet du niveau de sécurité 2 ne fonctionnent que s'ils accèdent aux ressources stockées dans le modèle de formulaire. 
    
- **3** Les membres du modèle objet sont accessibles uniquement par les formulaires entièrement fiables. 
    
- Chaque section des propriétés et méthodes de la référence du modèle objet InfoPath contient une section pour la sécurité qui spécifie le niveau de sécurité s'appliquant à ce membre du modèle objet.
    
- Le niveau de sécurité **1** est réservé à une utilisation future. 
    
## <a name="summary"></a>Résumé

Le tableau suivant récapitule les autorisations par défaut pour chaque méthode de déploiement de formulaires dans InfoPath. Les autorisations dépendent de la zone de sécurité du domaine d’où provient le modèle de formulaire.
  
|**Zone de sécurité**|**Déploiement**|**Autorisations par défaut**|
|:-----|:-----|:-----|
||**Basé sur l’URL** <br/> |**Basé sur l’URN** <br/> |**ActiveX marqués comme non sécurisés pour les scripts** <br/> |**Accès aux données d’autres domaines** <br/> |**Niveau de sécurité du modèle objet** <br/> |
|Sites sensibles  <br/> |N/A  <br/> |N/A  <br/> |N/A  <br/> |N/A  <br/> |N/A  <br/> |
|Internet  <br/> |X  <br/> ||Désactiver  <br/> |Désactiver  <br/> |2  <br/> |
|Intranet local  <br/> |X  <br/> ||Désactiver  <br/> |Invite  <br/> |2  <br/> |
|Sites approuvés  <br/> |X  <br/> ||Invite  <br/> |Activer  <br/> |2  <br/> |
|Ordinateur local  <br/> |X  <br/> |X  <br/> |Désactiver  <br/> |Invite  <br/> |2  <br/> |
|Formulaire entièrement fiable  <br/> |X (signé par un éditeur approuvé)  <br/> |X  <br/> |Activer  <br/> |Activer  <br/> |3  <br/> |
|Formulaire entièrement fiable  <br/> ||X  <br/> |Activer  <br/> |Activer  <br/> |3  <br/> |
|Restreint  <br/> ||X  <br/> |Pas d’ActiveX (à part une liste restreinte, codée en dur)  <br/> |Désactiver  <br/> |2  <br/> |
|Restreint  <br/> |X  <br/> ||Pas d’ActiveX (à part une liste restreinte, codée en dur)  <br/> |Désactiver  <br/> |2  <br/> |
|Restreint  <br/> |X  <br/> |X  <br/> |Pas d’ActiveX (à part une liste restreinte, codée en dur)  <br/> |Désactiver  <br/> |2  <br/> |
   
Pour plus d'informations sur les consignes générales de sécurité lors du développement de formulaires, voir [Consignes de sécurité pour développer des formulaires InfoPath](security-guidelines-for-developing-infopath-forms.md).
  
## <a name="understanding-other-security-features"></a>Description des autres fonctionnalités de sécurité

InfoPath fournit d’autres mesures de sécurité pour les formulaires, notamment la protection de la création grâce aux signatures numériques, la gestion de certaines opérations comme la fusion et l’envoi et l’approbation des formulaires installés. Les sections suivantes décrivent ces mesures de sécurité et indiquent où elles sont activées dans InfoPath.
  
## <a name="digital-signatures"></a>Signatures numériques

Les données stockées dans un formulaire peuvent être signées numériquement afin de garantir que le contenu ne sera pas modifié.
  
Vous configurez un formulaire pour qu'il utilise des signatures numériques en sélectionnant l'option **Autoriser la signature de l'ensemble du formulaire** ou **Autoriser la signature de certaines parties du formulaire** dans la section **Signatures numériques** de la boîte de dialogue **Options de formulaire**, accessible dans le mode Création InfoPath de Microsoft Office Backstage. Quand ils remplissent le formulaire, les utilisateurs peuvent signer et vérifier les formulaires en cliquant sur le bouton **Signer le formulaire** de l'onglet **Informations** de Microsoft Office Backstage. Lors de la réouverture du formulaire, l'utilisateur est averti si le contenu a été modifié. 
  
-  Les signatures numériques peuvent être activées pour l'ensemble du formulaire ou pour des ensembles de données spécifiques à signer séparément. 
    
- Vous pouvez décider de signer uniquement des sections spécifiques d'un formulaire plutôt que tout le formulaire.
    
- Vous pouvez choisir d'autoriser une ou plusieurs signatures. Vous pouvez également indiquer que la relation concerne chaque ensemble de données pouvant être signé. Par exemple, vous pouvez spécifier s'il s'agit de cosignatures parallèles ou si chaque nouvelle signature contresigne toutes les signatures précédentes.
    
- Vous pouvez utiliser le modèle objet InfoPath pour ajouter par la programmation des informations personnalisées au bloc de signature d'un formulaire entièrement fiable.
    
- Vous pouvez améliorer la sécurité des signatures numériques en collectant et en incluant des informations supplémentaires, par exemple un horodatage, comme preuve de non-répudiation. Étant donné que la preuve supplémentaire fait partie de la signature, il est impossible de la supprimer sans invalider la signature. À tout moment vous pouvez rappeler ou examiner les données collectées en cliquant sur une signature numérique dans le formulaire ou en sélectionnant une signature numérique dans la liste affichée dans la boîte de dialogue **Signatures numériques**. 
    
-  Vous pouvez insérer et voir une signature dans le document et afficher le formulaire tel qu'il sera proposé à chaque signataire. 
    
- La signature numérique contient également un instantané de la vue proposée au signataire à la signature du formulaire. Cet instantané est stocké en tant qu'image base64 au format PNG standard. 
    
## <a name="email-deployment"></a>Déploiement du courrier électronique

Vous pouvez déployer vos modèles de formulaire en tant que pièces jointes à un message électronique et les déplacer d’un emplacement à un autre. Ce mode de déploiement est un moyen simple et efficace de distribuer des formulaires à vos collègues de bureau et de déployer des formulaires auprès d'utilisateurs distants.
  
Vous pouvez signer numériquement un modèle de formulaire que vous créez, puis lui définir le niveau de sécurité Confiance totale. En outre, les formulaires entièrement fiables signés, lorsqu’ils sont déployés en tant que pièces jointes, peuvent être mis à jour plus facilement et plus efficacement.
  
Tous les formulaires du module de création d'InfoPath sont créés avec une identité. Ces informations permettent à InfoPath d'associer des formulaires à des modèles de formulaire dans le cache et de récupérer des mises à jour pour ces formulaires quand elles sont publiées dans un emplacement partagé. Par défaut, InfoPath crée deux identités pour les modèles de formulaire : un ID de formulaire et un chemin d'accès (connu également en tant qu'attribut **publishURL**). Vous trouverez plus d’informations sur le déploiement du courrier électronique dans la rubrique Niveaux de sécurité, Déploiement de messagerie électronique et [Modèles de formulaires distants.](security-levels-email-deployment-and-remote-form-templates.md)
  
## <a name="activex-controls"></a>Contrôles ActiveX

InfoPath prend en charge l'hébergement des contrôles ActiveX dans les formulaires qui sont ouverts dans l'éditeur InfoPath. Les contrôles ActiveX peuvent être préexistants (avec certaines contraintes) ou être écrits spécifiquement pour être utilisés avec InfoPath. ActiveX contrôles utilisés dans les formulaires InfoPath ne sont pas téléchargés automatiquement à partir de sites web. Au lieu de ça, les fichiers CAB des contrôles ActiveX qui ne sont pas déjà présents sur l'ordinateur de l'utilisateur doivent être ajoutés dans le fichier du modèle de formulaire.
  
Quand un contrôle ActiveX est utilisé dans un formulaire alors qu'il n'est pas inscrit sur l'ordinateur de l'utilisateur, le comportement à l'ouverture du formulaire dépend des paramètres de ce contrôle ActiveX dans le formulaire. Si aucun fichier CAB n'est inclus dans le fichier du modèle de formulaire, InfoPath n'ouvre pas le formulaire. Si le fichier CAB est présent dans le fichier du modèle de formulaire, InfoPath démarre un processus d'installation. Pour qu'InfoPath installe un fichier CAB, le fichier doit être signé et la signature doit émaner d'un éditeur approuvé. Si l'éditeur ne figure pas déjà dans la liste des éditeurs approuvés de l'utilisateur qui dispose d'un certificat (avec une chaîne d'approbation menant à une racine de certification approuvée), l'utilisateur sera invité à accepter ou refuser l'approbation de l'éditeur. Si l'utilisateur décide de ne pas approuver l'éditeur, le fichier CAB du contrôle ne sera pas installé et InfoPath n'ouvrira pas le formulaire.
  
> [!NOTE]
> [!REMARQUE] Les contrôles ActiveX doivent être marqués comme étant « Sûrs pour l'écriture de scripts » et « Sûrs pour l'initialisation avec des données non approuvées » pour être utilisés dans InfoPath. 
  
## <a name="net-security"></a>Sécurité .NET

Outre les niveaux de sécurité propres à InfoPath, les modèles de formulaire à code managé prennent également en charge d’autres fonctions de sécurité d’accès au code qui s’appliquent au code managé s’exécutant sous le Common Language Runtime (CLR) du Microsoft .NET Framework.
  
Si votre formulaire est entièrement fiable, il peut accéder automatiquement aux ressources à l'extérieur du modèle de formulaire. Tout assembly peut être utilisé dans le code de la logique métier. Vous pouvez personnaliser le jeu d'autorisations ajouté à un modèle de formulaire à code managé à l'aide de l'outil de configuration Microsoft .NET Framework ou de l'outil Stratégie de sécurité d'accès du code (Caspol.exe). InfoPath cherche un groupe de code prédéfini et applique le jeu d'autorisations qui est défini sous ce groupe dans le domaine d'applications (AppDomain) où le code managé est chargé et d'où il s'exécute. Des stratégies de sécurité .NET personnalisées doivent être déployées sur les ordinateurs clients où le modèle de formulaire à code managé s'exécutera.
  
Notez que la sécurité .NET n'accorde le jeu d'autorisations Internet qu'au code managé s'exécutant dans les sites de confiance Internet Explorer. Par conséquent, les formulaires InfoPath à code managé ne s'exécuteront pas s'ils sont publiés sur un Site de confiance.
  
## <a name="merging-forms"></a>Fusion des formulaires

Vous pouvez désactiver la fonction de fusion des formulaires pour empêcher les utilisateurs d'importer des données de plusieurs formulaires pour les placer dans un seul.
  
Pour activer ou désactiver la fusion des formulaires, utilisez la case à cocher **Activer la fusion de formulaires** dans la section **Avancé** de la boîte de dialogue **Options de formulaire**, accessible à partir de l'onglet **Informations** de Microsoft Office Backstage lors de la création du formulaire. Lorsque la fusion des formulaires est désactivée, les utilisateurs ne peuvent pas cliquer sur **Fusionner les formulaires** dans l'onglet **Partager** de Microsoft Office Backstage lors du remplissage d'un formulaire. 
  
## <a name="submitting-forms"></a>Envoi des formulaires

Vous pouvez désactiver la fonction d’envoi des formulaires pour empêcher les utilisateurs d’envoyer des formulaires.
  
Pour activer ou désactiver l'envoi de formulaires, utilisez la boîte de dialogue **Options d'envoi**, accessible en cliquant sur **Options d'envoi** dans le menu de l'onglet **Données** en mode de création. Lorsque la fonction d'envoi est désactivée, les utilisateurs ne peuvent pas cliquer sur **Envoyer** dans l'onglet **Accueil** lors du remplissage d'un formulaire. 
  

