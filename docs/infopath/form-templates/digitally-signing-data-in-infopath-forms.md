---
title: Signature numérique de données dans des formulaires InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7b396d9f-9a47-3170-367f-5d1f0144f927
description: Une signature numérique est un tampon électronique sécurisé, utilisant le chiffrement, pour l'authentification d'une macro ou d'un document. Une signature numérique confirme que les données proviennent bien du signataire et qu'elles n'ont pas été modifiées depuis la signature. Lorsque des documents ou certaines de leurs données sont signés, la signature est générée et ajoutée au document. De cette façon, les signatures accompagnent toujours les données signées.
ms.openlocfilehash: dc839d0751d2e7aeb6f9eaccc3a86ce95e5228e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782340"
---
# <a name="digitally-signing-data-in-infopath-forms"></a>Signature numérique de données dans des formulaires InfoPath

Une signature numérique est un tampon électronique sécurisé, utilisant le chiffrement, pour l'authentification d'une macro ou d'un document. Une signature numérique confirme que les données proviennent bien du signataire et qu'elles n'ont pas été modifiées depuis la signature. Lorsque des documents ou certaines de leurs données sont signés, la signature est générée et ajoutée au document. De cette façon, les signatures accompagnent toujours les données signées.
  
Pour signer des données, les utilisateurs doivent demander un certificat à une autorité de certification, puis l'utiliser pour créer des signatures numériques. L'autorité de certification gère le cycle de vie des certificats et des clés (publiques ou privées) nécessaires au chiffrement des données et à la création des signatures.
  
Les utilisateurs suivants du document doivent vérifier les signatures existantes, et en fonction du résultat de cette vérification, ils peuvent ajouter leur propre contribution et signer. Pour obtenir des résultats précis, le vérificateur doit approuver l'autorité de certification ayant émis le certificat utilisé pour la signature initiale du document.
  
Les signatures numériques XML sont conçues pour les transactions impliquant des données et des documents XML. La puissance des signatures XML réside dans la possibilité de signer uniquement des données spécifiques d'un document XML.
  
## <a name="types-of-digital-signatures-in-infopath-forms"></a>Types de signatures numériques dans les formulaires InfoPath

Microsoft InfoPath implémente des signatures numériques pour mieux protéger les données dans les formulaires InfoPath. Deux types de signatures numériques sont proposées dans InfoPath :
  
- Les signatures numériques qui garantissent l'intégrité des données et l'authenticité du modèle de formulaire (fichier .xsn)
    
- Les signatures numériques qui garantissent l'intégrité, l'authenticité et la prise en charge pour la non-répudiation des données des formulaires XML
    
Alors que la première catégorie de signatures ciblent le modèle de formulaire (fichier .xsn), la deuxième catégorie cible les données réelles entrées par l'utilisateur dans les formulaires InfoPath (fichiers .xml), où le créateur peut permettre aux utilisateurs de créer des signatures numériques pour tout le formulaire ou seulement pour des parties du formulaire. Il existe des différences fondamentales entre un modèle signé et un formulaire signé. Bien que ce document contienne des références aux modèles signés (comme autre méthode de création de formulaire s'exécutant comme étant entièrement fiable), il ne fournit pas de détails sur ce type de signature. Pour plus d'informations sur la signature des modèles de formulaire, voir [Déploiement de modèles de formulaire signés](deploying-signed-infopath-form-templates.md). Le présent document traite principalement de l'utilisation de formulaires XML XML signés. Les signatures numériques créées par InfoPath pour signer des données dans des formulaires XML respectent les normes des signatures numériques XML W3C. 
  
## <a name="digital-signatures-features"></a>Caractéristiques des signatures numériques

InfoPath propose une fonction élargie pour les signatures numériques, permettant aux développeurs des modèles de concevoir des formulaires flexibles acceptant des signatures numériques aussi bien pour tout le formulaire que pour des données spécifiques du formulaire. Alors que le fait de signer numériquement le formulaire entier crée toujours des contre-signatures pour le formulaire comme un tout, le fait d'en signer des parties offre davantage de souplesse dans le choix du type de relation entre les signatures ajoutées au même ensemble de données : il peut y avoir plusieurs signatures, des contre-signatures ou une seule signature possible.
  
Avec la signature, InfoPath ajoute également par défaut des informations de non-répudiation pour identifier les données que les utilisateurs ont vues dans la vue actuelle, ainsi que l'heure et d'autres paramètres de l'environnement tels qu'ils ont été définis au moment de la création de la signature. Les informations de non-répudiation peuvent être personnalisées, mais seules les données des nœuds de non-répudiation par défaut sont affichées dans la boîte de dialogue de non-répudiation.
  
Pour ajouter une signature, les utilisateurs doivent sélectionner l'ensemble de données qui sera signé. Cet ensemble est défini par le créateur du modèle de formulaire et utilisé pour signer les données lors du remplissage du formulaire. Pour chaque signature, les utilisateurs emploient un Assistant pour sélectionner l'ensemble des données à signer, en sélectionnant un certificat, en ajoutant des commentaires et en approuvant et validant la signature dans le formulaire.
  
Quand un utilisateur laisse le pointeur de la souris sur un contrôle qui contient des données signées, InfoPath affiche une indication visuelle pour signaler que les données sont signées et ne peuvent pas être modifiées. Les créateurs de modèles de formulaire peuvent décider d'afficher les signatures dans la vue avec les données signées pour que les utilisateurs accèdent facilement aux informations de non-répudiation.
  
## <a name="programmatic-support-for-digital-signatures"></a>Aide par la programmation pour les signatures numériques

Le modèle objet InfoPath inclut une prise en charge pour les signatures numériques, qui permet aux développeurs d'accéder via la programmation aux ensembles de données pouvant être signées qui sont définies dans le formulaire par le biais de la classe [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) , aux signatures affectées à chaque ensemble de données signées par le biais de la classe [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) et au certificat utilisé pour créer une signature par le biais de la classe [Certificate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.aspx) . De plus, le gestionnaire d'événements [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) peut être personnalisé dans les formulaires entièrement fiables, offrant ainsi la possibilité d'un traitement évolué des signatures numériques dans les formulaires InfoPath. 
  
## <a name="interoperability"></a>Interopérabilité

L'infrastructure des signatures numériques dans InfoPath a été conçue en utilisant la prise en charge des signatures numériques de MSXML5 pour que les signatures numériques InfoPath bénéficient d'une totale interopérabilité avec les signatures numériques MSXML5.
  
Les formulaires InfoPath signés et les signatures numériques créées par InfoPath fournissent également une totale interopérabilité avec les signatures numériques créées avec Microsoft .NET Framework (à compter de la version 1.1). Les signatures créées par InfoPath peuvent être vérifiées par les applications qui utilisent les classes de vérification .NET Framework. Les signatures créées pour les données hébergées dans des formulaires InfoPath par des applications conçues avec des classes de signatures numériques .NET Framework sont vérifiées sans problèmes par le mécanisme de signature d'InfoPath.
  
## <a name="see-also"></a>Voir aussi



[Utilisation de Signatures numériques](how-to-work-with-digital-signatures.md)

