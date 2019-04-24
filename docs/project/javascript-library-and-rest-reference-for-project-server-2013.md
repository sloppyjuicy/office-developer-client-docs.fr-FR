---
title: Bibliothèque JavaScript et référence REST pour Project Server
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 67b47b8b-d34b-4fad-af49-0c258c345ad2
description: La bibliothèque JavaScript et la référence REST de Project Server 2013 contiennent des informations sur le modèle d'objet JavaScript et l'interface REST que vous utilisez pour accéder aux fonctionnalités de Project Server. Vous pouvez utiliser ces API pour développer des applications Web internavigateurs, des compléments Project Professionnel 2013 et des applications pour les appareils autres que Windows qui accèdent à Project Server 2013 et Project online.
ms.openlocfilehash: fb58de1e3858a39f42cc9a643a7394cec191a462
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358106"
---
# <a name="javascript-library-and-rest-reference-for-project-server"></a>Bibliothèque JavaScript et référence REST pour Project Server

La bibliothèque JavaScript et la référence REST de Project Server 2013 contiennent des informations sur le modèle d'objet JavaScript et l'interface REST que vous utilisez pour accéder aux fonctionnalités de Project Server. Vous pouvez utiliser ces API pour développer des applications Web internavigateurs, des compléments Project Professionnel 2013 et des applications pour les appareils autres que Windows qui accèdent à Project Server 2013 et Project online.
  
> [!NOTE]
> Le modèle objet JavaScript et l'interface REST s'alignent sur le modèle objet côté client de Project Server (CSOM). Elles fournissent une fonctionnalité équivalente à l'espace de noms **Microsoft. ProjectServer. client** dans le CSOM. 
  
Vous pouvez accéder à la fonctionnalité de Project Server via le modèle objet JavaScript, qui est [](https://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx) défini dans l'espace `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.js` de noms PS du fichier. L'objet [ProjectContext](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx) dans l'espace de noms [PS](https://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx) est le point d'entrée du modèle objet JavaScript. 
  
> [!NOTE]
> Pour parcourir le modèle objet JavaScript et vous aider à déboguer, vous pouvez utiliser le fichier PS. Debug. js dans le même répertoire. Pour vous aider à développer sur un ordinateur distant, le [Téléchargement du kit de développement logiciel (SDK) Project 2013](https://www.microsoft.com/en-us/download/details.aspx?id=30435) inclut les assemblys .NET Framework pour le CSOM, ainsi que les fichiers PS. js et PS. Debug. js. 
  
Vous pouvez également accéder à la fonctionnalité de Project Server via l'interface REST. Le point d'entrée de l'interface REST est la ressource **ProjectServer** , à laquelle vous accédez à `https://ServerName/pwaName/_api/ProjectServer` l'aide de l'URI du point de terminaison. Par exemple, la requête suivante obtient les affectations dans le projet spécifié (remplacez _ServerName_ et _pwaName_, et modifiez le GUID pour qu'il corresponde à un projet).
  
`https://ServerName/pwaName/_api/ProjectServer/Projects('263fc8d7-427c-e111-92fc-00155d3ba208')/Assignments`

La ressource **ProjectServer** est décrite dans [ressources ProjectServer dans l'interface REST](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx#bk_ProjectServerResources). Les autres ressources REST sont décrites dans la documentation pour les objets et les membres JavaScript correspondants dans cette référence. Pour plus d'informations sur l'utilisation de REST, consultez la rubrique [Client-Side Object Model (CSOM) for Project Server](client-side-object-model-csom-for-project-2013.md) et [Programming using the SharePoint 2013 Rest service](https://msdn.microsoft.com/library/fp142385%28office.15%29.aspx).
  
## <a name="javascript-library-and-rest-reference-for-project-server"></a>Bibliothèque JavaScript et référence REST pour Project Server
<a name="pj15_JavaScriptAPIReference_PS"> </a>

- [Bibliothèque JavaScript PS. js et référence Rest](https://msdn.microsoft.com/library/5a140021-380a-d9e0-e36d-106df85f56d6%28Office.15%29.aspx) Contient des informations sur le modèle objet JavaScript et l'interface REST pour Project Server 2013. 
    
## <a name="see-also"></a>Voir aussi
<a name="bk_addresources"> </a>

- [Documentation du développeur Project 2013](project-2013-developer-documentation.md)   
- [Modèle objet côté client (CSOM) pour Project Server](client-side-object-model-csom-for-project-2013.md)   
- [Prise en main du modèle objet JavaScript](getting-started-with-the-project-server-2013-javascript-object-model.md)  
- [Utilisation des projets avec le modèle objet JavaScript](create-retrieve-update-delete-projects-using-project-server-javascript.md)
    

