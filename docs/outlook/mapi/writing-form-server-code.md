---
title: Écriture de code serveur de formulaire
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ff33badc-ceed-4364-b99c-8af3af83ceb6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a93e53261d56e452f38e38da427585cecccba405
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325793"
---
# <a name="writing-form-server-code"></a>Écriture de code serveur de formulaire

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Vous pouvez voir un serveur de formulaire comme suit : 
  
- Programme Win32 qui affiche une interface et gère les messages Windows à l’aide des mécanismes d’émission de messages Windows standard.
    
- Objet qui inscrit sa fabrique de classes avec OLE et est activé par les méthodes d’automatisation OLE.
    
- Objet MAPI qui suit les règles MAPI pour les interactions avec d’autres composants MAPI.
    
 Votre code doit gérer ces trois exigences générales simultanément. 
  
Pour plus d’informations sur l’inscription de la fabrique de classes de votre serveur de formulaires, voir la section COM et ActiveX Object Services dans le SDK Windows. La gestion des messages Windows et l’affichage d’une interface sont des techniques de programmation Windows standard qui n’ont aucune exigence particulière concernant les formulaires MAPI. Là encore, le SDK Windows dispose de détails sur la programmation Windows. Ce document contient ce que vous devez savoir pour implémenter les interfaces de formulaire MAPI requises et facultatives afin qu’elles suivent les règles MAPI pour les interactions avec d’autres composants MAPI, principalement le gestionnaire de formulaires MAPI et les applications clientes de messagerie.
  
Toutes les interfaces que vous pouvez utiliser lorsque vous implémentez des serveurs de formulaires sont dérivées , directement ou indirectement, de la classe de base OLE [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx). Cela signifie que toutes vos implémentations de ces interfaces doivent avoir des méthodes **QueryInterface,** **AddRef** et **Release.** Vous pouvez économiser beaucoup de travail si vous utilisez plusieurs héritages pour implémenter toutes les interfaces requises dans une nouvelle classe, afin que toutes les interfaces que vous utilisez peuvent partager une implémentation unique des méthodes **IUnknown** requises. Pour plus d’informations, voir les méthodes [IUnknown::AddRef,](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx)et [IUnknown::Release.](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) Il n’existe aucune considération particulière concernant les serveurs de formulaire MAPI pour ces méthodes. 
  
Bien que toutes les interfaces de formulaire MAPI ne soient pas obligatoires pour tous les serveurs de formulaires, les méthodes dans une interface donnée sont obligatoires. Autrement dit, si vous choisissez d’implémenter une interface particulière, vous devez implémenter toutes les méthodes de l’interface. Cette situation est différente de celle de certains autres composants MAPI, tels que les transports de messages. Heureusement, les méthodes dans les interfaces de formulaire MAPI sont relativement simples. Par conséquent, leur mise en œuvre n’est pas très lourde pour les développeurs.
  
Les interfaces de formulaire MAPI sont indépendantes du type d’outil de développement utilisé pour créer un serveur de formulaires. Cela permet de créer des formulaires à l’aide de différents outils de développement. La seule condition est que tous les serveurs de formulaires doivent prendre en charge les interfaces de formulaire MAPI requises.
  
Toutes les interfaces MAPI liées aux formulaires ne sont pas requises par tous les serveurs de formulaires. Les interfaces facultatives vous permettent d’implémenter certaines fonctions de formulaire avancées qui ne sont pas nécessaires à la plupart des serveurs de formulaires. Le tableau suivant répertorie les interfaces, leur utilisation et indique si vous devez les implémenter.
  
|**Interface**|**Description**|**État**|
|:-----|:-----|:-----|
|[IMAPIForm : IUnknown](imapiformiunknown.md) <br/> |Interface principale que les clients utilisent pour charger des serveurs de formulaires, exécuter des verbes de formulaire et arrêter des serveurs de formulaires. Il s’agit également de l’interface dérivée de OLE **IUnknown** qui est utilisée pour informer d’autres composants OLE concernant les interfaces implémentée par un objet de formulaire.  <br/> |Obligatoire  <br/> |
|[IPersistMessage : IUnknown](ipersistmessageiunknown.md) <br/> |Utilisé lors du chargement et de l’enregistrement des messages à partir d’objets de formulaire.  <br/> |Obligatoire  <br/> |
|[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md) <br/> |Utilisé par les objets de formulaire pour suivre l’état du client de messagerie et pour déterminer si l’objet formulaire est capable d’afficher le message suivant ou précédent dans un dossier.  <br/> |Facultatif  <br/> |
|[IClassFactory](https://msdn.microsoft.com/library/f624f833-2b69-43bc-92cd-c4ecbe6051c5%28Office.15%29.aspx) <br/> |Interface de fabrique de classe OLE utilisée par les objets de formulaire pour la conformité avec le mécanisme d’usine de classe OLE.  <br/> |Obligatoire  <br/> |
|[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md) <br/> |Utilisé si votre serveur de formulaires prend en charge plusieurs types de formulaires. Dans ce cas, l’interface **IMAPIFormFactory** permet aux applications clientes d’accéder aux interfaces **IClassFactory** multiples (une par type de formulaire que votre serveur de formulaires prend en charge) que votre serveur de formulaires doit également implémenter.  <br/> |Facultatif  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Développement de serveurs de formulaire MAPI](developing-mapi-form-servers.md)

