import React from 'react';
import { View, ActivityIndicator } from 'react-native';
import { WebView } from 'react-native-webview';
import { useRouter, useLocalSearchParams } from 'expo-router';
import { PhoneAuthProvider } from 'firebase/auth';
import { auth } from '@/config/firebase';

export default function RecaptchaScreen() {
  const router = useRouter();
  const { phone, name, gender } = useLocalSearchParams();

  const handleMessage = async (event: any) => {
    const token = event?.nativeEvent?.data;

    if (token) {
      try {
        const provider = new PhoneAuthProvider(auth);
        const verificationId = await provider.verifyPhoneNumber(phone as string, {
          type: 'recaptcha',
          token,
        });

        router.push({
          pathname: '/login',
          params: {
            phone: phone as string,
            name: name as string,
            gender: gender as string,
            verificationId,
            showVerification: 'true',
          },
        });
      } catch (error) {
        console.error('Phone verification failed:', error);
        router.replace('/login'); // fallback
      }
    }
  };

  return (
    <WebView
      source={{ uri: 'https://your-public-url.com/recaptcha.html' }} // Replace with actual hosted HTML
      javaScriptEnabled
      originWhitelist={['*']}
      onMessage={handleMessage}
      startInLoadingState
      renderLoading={() => (
        <View style={{ flex: 1, justifyContent: 'center', alignItems: 'center' }}>
          <ActivityIndicator size="large" />
        </View>
      )}
    />
  );
}
