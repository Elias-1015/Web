# Web
Saint Aloysius Gonzaga 

import Navigation from '@/components/Navigation';
import Footer from '@/components/Footer';
import { Card, CardContent, CardDescription, CardHeader, CardTitle } from '@/components/ui/card';
import { Badge } from '@/components/ui/badge';
import { Heart, Users, Church, Leaf, Target, Eye } from 'lucide-react';

const About = () => {
  const values = [
    {
      icon: Church,
      title: 'Faith',
      description: 'Rooted in Catholic teachings and dedicated to spiritual growth',
    },
    {
      icon: Users,
      title: 'Unity',
      description: 'Building strong bonds within our community and beyond',
    },
    {
      icon: Heart,
      title: 'Service',
      description: 'Serving those in need with compassion and dedication',
    },
    {
      icon: Heart,
      title: 'Love',
      description: 'Sharing Christ\'s love through our actions and words',
    },
    {
      icon: Leaf,
      title: 'Stewardship',
      description: 'Caring for God\'s creation and our community resources',
    },
  ];

  return (
    <div className="min-h-screen bg-background">
      <Navigation />
      
      {/* Hero Section */}
      <section className="bg-primary text-primary-foreground py-16">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="text-center">
            <h1 className="text-4xl md:text-5xl font-serif font-bold mb-6">About Us</h1>
            <p className="text-xl max-w-3xl mx-auto opacity-90">
              Learn about our community, mission, and the values that guide us
            </p>
          </div>
        </div>
      </section>

      {/* About Content */}
      <section className="py-16">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center mb-16">
            <div>
              <h2 className="text-3xl font-serif font-bold mb-6">Our Story</h2>
              <div className="space-y-4 text-lg text-muted-foreground">
                <p>
                  YCA Saint Aloysius Gonzaga Sigowet was founded as a Small Christian Community (SCC) 
                  under St. Joseph the Worker Kapyemit Parish in the Matunda Deanery, Eldoret Diocese. 
                  We are named after Saint Aloysius Gonzaga, the patron saint of youth, who exemplified 
                  purity, dedication, and service to God.
                </p>
                <p>
                  Our community began with a small group of dedicated young adults who shared a vision 
                  of active participation in the Catholic Church while serving our local community. 
                  Today, we are proud to have over 25 active members committed to our mission.
                </p>
                <p>
                  We organize regular activities including community service, environmental conservation, 
                  youth formation, and support for those in need. Our annual Lodwar Mission represents 
                  our commitment to reaching out beyond our parish boundaries.
                </p>
              </div>
            </div>
            <div className="bg-muted rounded-lg p-8">
              <h3 className="text-2xl font-serif font-bold mb-4">Quick Facts</h3>
              <div className="space-y-4">
                <div className="flex justify-between">
                  <span className="font-medium">Founded:</span>
                  <Badge variant="secondary">2020</Badge>
                </div>
                <div className="flex justify-between">
                  <span className="font-medium">Members:</span>
                  <Badge variant="secondary">25+ Active</Badge>
                </div>
                <div className="flex justify-between">
                  <span className="font-medium">Parish:</span>
                  <Badge variant="secondary">Kapyemit</Badge>
                </div>
                <div className="flex justify-between">
                  <span className="font-medium">Deanery:</span>
                  <Badge variant="secondary">Matunda</Badge>
                </div>
                <div className="flex justify-between">
                  <span className="font-medium">Diocese:</span>
                  <Badge variant="secondary">Eldoret</Badge>
                </div>
              </div>
            </div>
          </div>

          {/* Mission and Vision */}
          <div className="grid grid-cols-1 md:grid-cols-2 gap-8 mb-16">
            <Card className="border-primary/20">
              <CardHeader>
                <div className="flex items-center space-x-2 mb-2">
                  <Target className="h-6 w-6 text-primary" />
                  <CardTitle className="text-2xl">Our Mission</CardTitle>
                </div>
              </CardHeader>
              <CardContent>
                <p className="text-lg leading-relaxed">
                  To nurture the spiritual, social, and economic growth of young adults through 
                  active participation in the Catholic Church, community service, and the 
                  formation of strong Christian values.
                </p>
              </CardContent>
            </Card>

            <Card className="border-primary/20">
              <CardHeader>
                <div className="flex items-center space-x-2 mb-2">
                  <Eye className="h-6 w-6 text-primary" />
                  <CardTitle className="text-2xl">Our Vision</CardTitle>
                </div>
              </CardHeader>
              <CardContent>
                <p className="text-lg leading-relaxed">
                  A strong, united Catholic youth community empowered to transform society 
                  through faith, love, and service, following the example of Saint Aloysius Gonzaga.
                </p>
              </CardContent>
            </Card>
          </div>

          {/* Core Values */}
          <div className="mb-16">
            <h2 className="text-3xl font-serif font-bold text-center mb-12">Our Core Values</h2>
            <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
              {values.map((value, index) => {
                const IconComponent = value.icon;
                return (
                  <Card key={index} className="text-center hover:shadow-lg transition-shadow">
                    <CardHeader>
                      <div className="mx-auto w-16 h-16 catholic-gradient rounded-full flex items-center justify-center mb-4">
                        <IconComponent className="h-8 w-8 text-white" />
                      </div>
                      <CardTitle className="text-xl">{value.title}</CardTitle>
                    </CardHeader>
                    <CardContent>
                      <p className="text-muted-foreground">{value.description}</p>
                    </CardContent>
                  </Card>
                );
              })}
            </div>
          </div>

          {/* Saint Aloysius Gonzaga */}
          <Card className="bg-muted/50">
            <CardHeader>
              <CardTitle className="text-2xl text-center">About Saint Aloysius Gonzaga</CardTitle>
            </CardHeader>
            <CardContent className="text-center">
              <p className="text-lg mb-4">
                Saint Aloysius Gonzaga (1568-1591) was an Italian aristocrat who became a Jesuit scholastic. 
                He is the patron saint of young students, Christian youth, and plague victims.
              </p>
              <p className="text-muted-foreground">
                Known for his deep devotion to God, purity of heart, and service to the poor and sick, 
                Saint Aloysius died at age 23 while caring for plague victims in Rome. His feast day 
                is celebrated on June 21st, which we honor annually as our special celebration day.
              </p>
            </CardContent>
          </Card>
        </div>
      </section>

      <Footer />
    </div>
  );
};

export default About;
